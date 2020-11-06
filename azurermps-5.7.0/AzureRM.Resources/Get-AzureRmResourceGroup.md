---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: f3924115d68d7e844503e076a214c95bf3d2239d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502486"
---
# Get-AzureRmResourceGroup

## Synopsis
Ruft Ressourcengruppen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### GetByResourceGroupName (Standard)
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmResourceGroup** " ruft Azure-Ressourcengruppen im aktuellen Abonnement ab.
Sie können alle Ressourcengruppen abrufen oder eine Ressourcengruppe nach Namen oder nach anderen Eigenschaften angeben.
Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.

Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzureRmResourceGroup-Cmdlet.

## Beispiele

### Beispiel 1: Abrufen einer Ressourcengruppe nach Namen
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen EngineerBlog ab.

### Beispiel 2: Abrufen aller Kategorien einer Ressourcengruppe
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

Dieser Befehl ruft die Ressourcengruppe mit dem Namen ContosoRG ab und zeigt die Tags an, die dieser Gruppe zugeordnet sind.

### Beispiel 3: Anzeigen der Ressourcengruppen nach Standort
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Beispiel 4: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Speicherort
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Beispiel 5: Anzeigen der Ressourcengruppen, deren Namen mit Webserver beginnen
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

## Parameter

### -ApiVersion
Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.
Sie können eine andere Version als die Standard Version angeben.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die ID der Ressourcengruppe an, die abgerufen werden soll.
Platzhalterzeichen sind nicht zulässig.

```yaml
Type: String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Gibt den Speicherort der Ressourcengruppe an, die abgerufen werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Ressourcengruppe an, die abgerufen werden soll.
Platzhalterzeichen sind nicht zulässig.

```yaml
Type: String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Zeichenfolge
Sie können die Eingabe an das Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.

## Ausgaben

### Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup
Dieses Cmdlet gibt Ressourcengruppen zurück.

## Notizen

## Verwandte Links

[Neu – AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Satz-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


