---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementNamedValue.md
ms.openlocfilehash: d3902a085ae870034bbb0fbc668d55166b7fe61c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381701"
---
# Set-AzApiManagementNamedValue

## SYNOPSIS
Ändert einen benannten API-Verwaltungswert.

## SYNTAX

```
Set-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Set-AzApiManagementNamedValue"** ändert einen benannten Azure API-Verwaltungswert.

## BEISPIELE

### Beispiel 1: Ändern der Tags für den benannten Wert
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -Tags $Tags -PassThru
```

Der erste Befehl weist der Variablen $Tags Werte zu.
Der zweite Befehl ändert den benannten Wert, der die ID Property11 hat.
Der Befehl weist die Zeichenfolgen in $Tags als Tags für den benannten Wert zu.

### Beispiel 2: Ändern des benannten Werts auf einen geheimen Wert
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property12" -Secret $True -PassThru
```

Mit diesem Befehl wird der benannte Wert in "Verschlüsselt" geändert.

### Beispiel 3

Ändert einen benannten API-Verwaltungswert. (automatisch generiert)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzApiManagementNamedValue -Context <PsApiManagementContext> -Name 'ContosoApi' -NamedValueId 'Property11' -Secret $true -Tag <String[]> -Value 'Property Value'
```

## PARAMETERS

### -Context
Instanz von PsApiManagementContext.
Dieser Parameter ist erforderlich.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name des benannten Werts.
Die maximale Länge beträgt 100 Zeichen.
Sie darf nur Buchstaben, Ziffern, Bindestriche und Unterstriche enthalten.
Dieser Parameter ist optional.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NamedValueId
Bezeichner des zu aktualisierende benannten Werts.
Dieser Parameter ist obligatorisch.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Wenn angegeben, wird eine Instanz des Typs "Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty", der die geänderte Eigenschaft darstellt, in die Ausgabe geschrieben.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Gibt an, ob der benannte Wert ein geheimer Wert ist und sein Wert verschlüsselt werden soll.
Dieser Parameter ist optional.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Dem benannten Wert zugeordnete Tags.
Dieser Parameter ist optional.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Value
Wert des benannten Werts.
Kann Richtlinienausdrücke enthalten.
Die maximale Länge beträgt 1.000 Zeichen.
Er darf nicht leer sein oder nur aus Leerzeichen bestehen.
Dieser Parameter ist optional.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String[]

### System.Management.Automation.SwitchParameter

## AUSGABEN

### Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
