# Ioc Populate
Vit.Ioc��DependencyInjection���е���չ������ͨ�������ļ�ʵ������ע�롣


## appsettings.json demo

``` json
//appsettings.json demo
{"Ioc": {
    "Services": [
      {
        /* �������ڡ���Ϊ Scoped��Singleton��Transient��Ĭ��Scoped */
        "Lifetime": "Scoped",
        "Service": "Cy.NetCore.Common.Interfaces.IService,Cy.NetCore.Common.Interfaces"
      },
      {
        /* �������ڡ���Ϊ Scoped��Singleton��Transient��Ĭ��Scoped */
        "Lifetime": "Scoped",
        "Service": "Cy.NetCore.Common.Interfaces.IService,Cy.NetCore.Common.Interfaces",
        "Implementation": "Cy.NetCore.Common.DataBase.ServiceImpl.ServiceA,Cy.NetCore.Common.DataBase"
      },
      {
        /* �������ڡ���Ϊ Scoped��Singleton��Transient��Ĭ��Scoped */
        "Lifetime": "Scoped",
        "Service": {

          /* �ڴ�Assembly�ļ��в�����(�� Vit.Core.dll)(assemblyFile��assemblyName ָ����һ����) */
          "assemblyFile": "Did.SersLoader.Demo.dll",

          /* �ڴ�Assembly�в�����(�� Vit.Core)(assemblyFile��assemblyName ָ����һ����) */
          //"assemblyName": "Did.SersLoader.Demo",

          /* ��̬���ص����� */
          "className": "Bearer"

        },
        "Implementation": {

          /* �ڴ�Assembly�ļ��в�����(�� Vit.Core.dll)(assemblyFile��assemblyName ָ����һ����) */
          "assemblyFile": "Did.SersLoader.Demo.dll",

          /* �ڴ�Assembly�в�����(�� Vit.Core)(assemblyFile��assemblyName ָ����һ����) */
          //"assemblyName": "Did.SersLoader.Demo",

          /* ��̬���ص����� */
          "className": "Bearer",

          "Invoke": [
            {
              "Name": "fieldName",
              "Value": "lith"
            },
            {
              "Name": "prpertyName",
              "Value": 12
            },
            {
              "Name": "methodName",
              "Params": [ 1, "12" ]
            }
          ]
        }
      }
    ]
  }
}
```