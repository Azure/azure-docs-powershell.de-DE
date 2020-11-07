---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: d09031270e61be80228003ae2a9ae47a5ce5ac74
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843416"
---
# Get-AzResourceGroup

## Synopsis
Ruft Ressourcengruppen ab.

## Syntax

### GetByResourceGroupName (Standard)
```
Get-AzResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzResourceGroup** " ruft Azure-Ressourcengruppen im aktuellen Abonnement ab.
Sie können alle Ressourcengruppen abrufen oder eine Ressourcengruppe nach Namen oder nach anderen Eigenschaften angeben.
Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.
Weitere Informationen zu Azure-Ressourcen und Azure-Ressourcengruppen finden Sie unter New-AzResourceGroup-Cmdlet.

## Beispiele

### Beispiel 1: Abrufen einer Ressourcengruppe nach Namen
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen EngineerBlog ab.

### Beispiel 2: Abrufen aller Kategorien einer Ressourcengruppe
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

Dieser Befehl ruft die Ressourcengruppe mit dem Namen ContosoRG ab und zeigt die Tags an, die dieser Gruppe zugeordnet sind.

### Beispiel 3: Anzeigen der Ressourcengruppen nach Standort
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Beispiel 4: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Speicherort
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Beispiel 5: Anzeigen der Ressourcengruppen, deren Namen mit Webserver beginnen
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

## Parameter

### -ApiVersion
Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.
Sie können eine andere Version als die Standard Version angeben.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Ressourcengruppe an, die abgerufen werden soll. Dieser Parameter unterstützt Platzhalter am Anfang und/oder am Ende der Zeichenfolge.

```yaml
Type: System.String
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Das Tag Hashtable zum Filtern von Ressourcengruppen nach.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. ResourceManagement. PSResourceGroup

## Notizen

## Verwandte Links

[Neu – AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Satz-AzResourceGroup](./Set-AzResourceGroup.md)


