---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 7cffc754e2662216aef10f163601e5d5a5339663
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291022"
---
# Restore-AzDeletedWebApp

## SYNOPSIS
Stellt eine gelöschte Web App in einer neuen oder vorhandenen Web App wieder zur Verfügung.

## SYNTAX

### FromDeletedResourceName (Standard)
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FromDeletedApp
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## BESCHREIBUNG
Mit **dem Cmdlet "Restore-AzDeletedWebApp"** wird eine gelöschte Web App wiederhergestellt. Die durch TargetResourceGroupName, TargetName und TargetSlot angegebene Web App wird mit den Inhalten und Einstellungen der gelöschten Web App überschrieben. Wenn die Zielparameter nicht angegeben werden, werden sie automatisch mit der Ressourcengruppe, dem Namen und dem Platz der gelöschten Web App ausgefüllt. Wenn die Ziel-Web-App nicht vorhanden ist, wird sie automatisch in dem von TargetAppServicePlanName angegebenen App-Dienstplan erstellt. Der Parameter "RestoreContentOnly" kann verwendet werden, um nur die Dateien der gelöschten App ohne die Einstellungen der App wiederherzustellen.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

Stellt eine gelöschte App namens "ContosoApp" wieder dar, die zur Ressourcengruppe "Default-Web-WestUS" gehört. Im App-Serviceplan mit dem Namen "ContosoPlan" wird eine neue App mit demselben Namen und derselben Ressourcengruppe erstellt, und die Dateien und Einstellungen der gelöschten App werden wiederhergestellt.

### Beispiel 2
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

Stellt den Stagingplatz einer gelöschten App namens "ContosoApp" wieder dar, die zur Ressourcengruppe "Default-Web-WestUS" gehört. Die Zur Ressourcengruppe "Default-Web-EastUS" gehörende Web-App namens "ContosoRestore" wird überschrieben. Die gelöschten Web -App-Einstellungen werden nicht wiederhergestellt.

###Beispiel 3
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

Falls es zwei gelöschte Apps mit demselben Namen (ContosoApp) gibt, erhalten wir Details zu beiden Websites und stellen die App mit der App Ihrer Wahl wieder zur Verfügung, indem wir "Mit ID wiederherstellen" aufrufen.

###Beispiel 4
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

Falls zwei gelöschte Apps mit demselben Namen (ContosoApp) vorhanden sind, erhalten wir Details zu den Websites und stellen die App mit der App Ihrer Wahl wieder her, indem wir die Wiederherstellung mit InputObject(Deletedsite)-Details aufrufen. 

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

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

### -DeletedId
Die ID der gelöschten Azure Web App.

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Stellen Sie die Wiederherstellung ohne Bestätigungsaufforderung vor.

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

### -InputObject
Die gelöschte Azure Web App.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Location
Der Speicherort der gelöschten Azure Web App.

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der gelöschten Azure Web App.

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe der gelöschten Azure Web App.

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreContentOnly
Wiederherstellen der Web-App-Dateien, aber nicht Wiederherstellen der Einstellungen.

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

### -Slot
Der gelöschte Azure Web App-Slot.

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAppServicePlanName
Der App-Dienstplan für die neue Azure Web App.

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

### -TargetName
Der Name der neuen Azure Web App.

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

### -TargetResourceGroupName
Die Ressourcengruppe, die die neue Azure Web App enthält.

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

### -TargetSlot
Der Name des neuen Azure Web App-Slot.

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

### -UseDisasterRecovery
Zum Wiederherstellen einer gelöschten App aus einer Skalierungseinheit, die offline ist.

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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp

## AUSGABEN

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzDeletedWebApp](./Get-AzDeletedWebApp.md)