# Mediator Pattern

## Мотивация
* Обект, който енкапсулира как набор от обекти си взаимодействат. Този модел насърчава разхлабването на връзките между обектите,
като не им позволява да се реферират пряко един друг. 

## Имплементация
```c#
//IVSR: Mediator pattern
public interface IComponent
{
    void SetState(object state);
}

public class Component1 : IComponent
{
    #region IComponent Members

    public void SetState(object state)
    {
        //Do Nothing
        throw new NotImplementedException();
    }

    #endregion
}

public class Component2 : IComponent
{
    #region IComponent Members

    public void SetState(object state)
    {
        //Do nothing
        throw new NotImplementedException();
    }

    #endregion
}

// Mediates the common tasks
public class Mediator
{
    public IComponent Component1
    {
        get;
        set;
    }
    public IComponent Component2
    {
        get;
        set;
    }

    public void ChangeState(object state)
    {
        this.Component1.SetState(state);
        this.Component2.SetState(state);
    }
}
```

## UML диаграма
![](https://dzone.com/sites/all/files/mediator_pattern.png)
