---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 553a9561939ffcef3337b0c13d384c5f5f47340e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664949"
---
# Remove-AzureRmWebAppSSLBinding

## Synopsis
Entfernt eine SSL-Bindung aus einem hochgeladenen Zertifikat.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### S1
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmWebAppSSLBinding** entfernt eine SSL-Bindung (Secure Sockets Layer) aus einer Azure Web App.
SSL-Bindungen werden verwendet, um eine Web-App einem Zertifikat zuzuordnen.

## Beispiele

### Beispiel 1: Entfernen einer SSL-Bindung für eine Web-App
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Dieser Befehl entfernt die SSL-Bindung für das Web App-ContosoWebApp.
Da der *DeleteCertificate* -Parameter nicht enthalten ist, wird das Zertifikat gelöscht, wenn keine SSL-Bindungen mehr vorhanden sind.

### Beispiel 2: Entfernen einer SSL-Bindung, ohne das Zertifikat zu entfernen
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Ähnlich wie Beispiel 1 entfernt dieser Befehl auch die SSL-Bindung für das Web App-ContosoWebApp.
In diesem Fall ist der *DeleteCertificate* -Parameter jedoch enthalten, und der Parameterwert ist auf $false eingestellt.
Das bedeutet, dass das Zertifikat nicht gelöscht wird, unabhängig davon, ob SSL-Bindungen vorhanden sind oder nicht.

### Beispiel 3: Verwenden eines Objektverweises zum Entfernen einer SSL-Bindung
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

In diesem Beispiel wird ein Objektverweis auf die Web App-Website verwendet, um die SSL-Bindung für eine Web-App zu entfernen.

Der erste Befehl verwendet das Get-AzureRmWebApp-Cmdlet, um einen Objektverweis auf die Web-App mit dem Namen ContosoWebApp zu erstellen.
Dieser Objektverweis wird in einer Variablen mit dem Namen $webapp gespeichert.

Der zweite Befehl verwendet den Objektverweis und das Cmdlet **Remove-AzureRmWebAppSSLBinding** , um die SSL-Bindung zu entfernen.

## Parameter

### -DeleteCertificate
Gibt die Aktion an, die durchgeführt werden soll, wenn die zu entfernende SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.
Wenn *DeleteCertificate* auf $false eingestellt ist, wird das Zertifikat nicht gelöscht, wenn die Bindung gelöscht wird.
Wenn *DeleteCertificate* auf $true gesetzt ist oder nicht im Befehl enthalten ist, wird das Zertifikat zusammen mit der SSL-Bindung gelöscht.

Das Zertifikat wird nur gelöscht, wenn die zu entfernenden SSL-Bindung die einzige vom Zertifikat verwendete Bindung ist.
Wenn das Zertifikat mehr als eine Bindung aufweist, wird das Zertifikat unabhängig vom Wert des *DeleteCertificate* -Parameters nicht entfernt.

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
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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
Gibt den Namen der Web-App an.

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

Im gleichen Befehl können *ResourceGroupName* Sie den Parameter ResourceGroupName *und den Parameter* "Webanwendung" nicht verwenden.

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
Gibt den Bereitstellungs Steckplatz für Web App an.
Verwenden Sie das Get-AzureRMWebAppSlot-Cmdlet, um einen Bereitstellungs Steckplatz abzurufen.

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

### -Webbasierte
Gibt eine Web-App an.
Verwenden Sie das Get-AzureRmWebApp-Cmdlet, um eine Web-App abzurufen.

Sie können den Webanwendungs Parameter nicht im gleichen Befehl *wie der* *ResourceGroupName* -Parameter und/oder den Webanwendungs *-Parameter verwenden* .

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Webbasierter
Gibt den Namen der Web-App an.

Im gleichen Befehl können *Sie den Parameter "* Webanwendungs" und *den "Webanwendungs Parameter"* nicht verwenden.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Website
Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[Neu – AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


