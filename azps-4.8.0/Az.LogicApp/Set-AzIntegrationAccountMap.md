---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009780"
---
# Set-AzIntegrationAccountMap

## Synopsis
Ändert eine Integration-Kontozuordnung.

## Syntax

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzIntegrationAccountMap** " ändert eine Integration-Kontozuordnung.
Dieses Cmdlet gibt ein Objekt zurück, das die Integrations Kontozuordnung darstellt.
Geben Sie den Namen des Integrations Kontos, den Ressourcengruppennamen und den Kartennamen an.
Dieses Modul unterstützt dynamische Parameter.
Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.
Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.
Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.

## Beispiele

### Beispiel 1: Ändern einer Integration-Kontozuordnung
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

Mit diesem Befehl wird die Integrations Kontozuordnung in der angegebenen Ressourcengruppe geändert.
Der Befehl gibt eine Kartendefinition an, die von einem vorherigen Befehl in der $MapContent Variablen gespeichert ist.

### Beispiel 2

Ändert eine Integration-Kontozuordnung. automatisch

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## Parameter

### -ContentType
Gibt einen Inhaltstyp für die Integrations Kontozuordnung an.
Dieses Cmdlet unterstützt Application/XML als Karten Inhaltstyp.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapDefinition
Gibt ein Definitionsobjekt für die Integration-Kontozuordnung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapFilePath
Gibt den Dateipfad einer Definition für die Integrations Kontozuordnung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapName
Gibt den Namen einer Integrations Kontozuordnung an.

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

### -MapType
Gibt den Typ für die Integrations Kontozuordnung an.
Dieses Cmdlet unterstützt XSLT als Kartentyp.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metadaten
Gibt ein Metadatenobjekt für die Zuordnung an.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Integrations Kontos an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an.

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

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap

## Notizen

## Verwandte Links

[Get-AzIntegrationAccountMap](./Get-AzIntegrationAccountMap.md)

[Neu – AzIntegrationAccountMap](./New-AzIntegrationAccountMap.md)

[Remove-AzIntegrationAccountMap](./Remove-AzIntegrationAccountMap.md)


