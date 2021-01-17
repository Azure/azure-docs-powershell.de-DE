---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460372"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
Entfernt eine SSL-Bindung aus einem hochgeladenen Zertifikat.

## SYNTAX

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Remove-AzWebAppSSLBinding"** entfernt eine Secure Sockets Layer (SSL)-Bindung aus einer Azure Web App.
SSL-Bindungen werden verwendet, um eine Web App einem Zertifikat zuzuordnen.

## BEISPIELE

### Beispiel 1: Entfernen einer SSL-Bindung für eine Web App
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Mit diesem Befehl wird die SSL-Bindung für die Web App ContosoWebApp entfernt.
Da der *Parameter "DeleteCertificate"* nicht enthalten ist, wird das Zertifikat gelöscht, wenn es keine SSL-Bindungen mehr enthält.

### Beispiel 2: Entfernen einer SSL-Bindung ohne Entfernen des Zertifikats
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Ähnlich wie in Beispiel 1 entfernt dieser Befehl auch die SSL-Bindung für die Web App ContosoWebApp.
In diesem Fall ist jedoch der *Parameter "DeleteCertificate"* enthalten, und der Parameterwert wird auf "$False.
Das bedeutet, dass das Zertifikat nicht gelöscht wird, unabhängig davon, ob es über SSL-Bindungen verfügt oder nicht.

### Beispiel 3: Verwenden eines Objektverweises zum Entfernen einer SSL-Bindung
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

In diesem Beispiel wird ein Objektverweis auf die Web App-Website verwendet, um die -SSL-Bindung für eine Web App zu entfernen.
Der erste Befehl verwendet das Get-AzWebApp Cmdlet, um einen Objektverweis auf die Web App namens "ContosoWebApp" zu erstellen.
Dieser Objektverweis wird in einer Variablen mit dem Namen $WebApp.
Der zweite Befehl verwendet den Objektverweis und das **Cmdlet "Remove-AzWebAppSSLBinding"** zum Entfernen der SSL-Bindung.

## PARAMETERS

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

### -DeleteCertificate
Gibt die Aktion an, die erfolgt, wenn die ssl-Bindung, die entfernt wird, die einzige vom Zertifikat verwendete Bindung ist.
Wenn *DeleteCertificate* auf $False festgelegt ist, wird das Zertifikat beim Löschen der Bindung nicht gelöscht.
Wenn *DeleteCertificate* auf $True oder nicht im Befehl enthalten ist, wird das Zertifikat zusammen mit der SSL-Bindung gelöscht.
Das Zertifikat wird nur gelöscht, wenn die zu entfernende SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.
Wenn das Zertifikat mehrere Bindungen enthält, wird das Zertifikat unabhängig vom Wert des Parameters *"DeleteCertificate" nicht* entfernt.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Web App an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.
Sie können den Parameter *"ResourceGroupName"* und den Parameter *"WebApp"* nicht im gleichen Befehl verwenden.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Gibt den Bereitstellungsplatz für Web App an.
Um einen Bereitstellungsplatz zu erhalten, verwenden Sie das Get-AzWebAppSlot Cmdlet.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Gibt eine Web App an.
Um eine Web App zu erhalten, verwenden Sie das Get-AzWebApp Cmdlet.
Sie können den Parameter *"WebApp"* nicht in demselben Befehl wie den *Parameter "ResourceGroupName"* und/oder *"WebAppName" verwenden.*

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Gibt den Namen der Web App an.
Sie können den Parameter *"WebAppName"* und den Parameter *"WebApp" nicht* im gleichen Befehl verwenden.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Waswenn
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## AUSGABEN

### System.Void

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


