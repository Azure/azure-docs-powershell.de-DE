---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D84F81A-F6B5-413D-B349-50947FCD5CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpAddress.md
ms.openlocfilehash: 8c48c7ec1f651348309c012275287bd88dd42bcc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151588"
---
# New-AzPublicIpAddress

## SYNOPSIS
Erstellt eine öffentliche IP-Adresse.

## SYNTAX

```
New-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -AllocationMethod <String> [-IpAddressVersion <String>] [-DomainNameLabel <String>]
 [-IpTag <PSPublicIpTag[]>] [-PublicIpPrefix <PSPublicIpPrefix>] [-ReverseFqdn <String>]
 [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzPublicIpAddress"** erstellt eine öffentliche IP-Adresse.

## BEISPIELE

### Beispiel 1: Erstellen einer neuen öffentlichen IP-Adresse
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
```

Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll. Dieser Ressource wird sofort eine öffentliche IP-Adresse zugewiesen, da "-AllocationMethod" als "Statisch" angegeben wird. Wenn sie als "Dynamisch" angegeben ist, wird eine öffentliche IP-Adresse nur zugeordnet, wenn Sie die zugeordnete Ressource (z. B. eine VM oder einen Lastenausgleich) starten (oder erstellen).

### Beispiel 2: Erstellen einer öffentlichen IP-Adresse mit einem umgekehrten FQDN
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -ReverseFqdn $customFqdn
```

Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Mit dem Parameter "-ReverseFqdn" erstellt Azure einen DNS -PTR-Eintrag (Reverse-Lookup) für die öffentliche IP-Adresse, die dieser Ressource zugeordnet ist, und führt auf die $customFqdn, die im Befehl angegeben ist. Als Voraussetzung sollte für die $customFqdn (z. B. webapp.contoso.com) ein DNS-CNAME-Eintrag (Forward-Lookup) vorhanden sein, der auf $dnsPrefix.$location.cloudapp.azure.com verweisen soll.

### Beispiel 3: Erstellen einer neuen öffentlichen #A0 mit IpTag
```powershell
$ipTag = New-AzPublicIpTag -IpTagType "FirstPartyUsage" -Tag "/Sql"
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location -IpTags $ipTag
```

Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll. Dieser Ressource wird sofort eine öffentliche IP-Adresse zugewiesen, da "-AllocationMethod" als "Statisch" angegeben wird. Wenn sie als "Dynamisch" angegeben ist, wird eine öffentliche IP-Adresse nur zugeordnet, wenn Sie die zugeordnete Ressource (z. B. eine VM oder einen Lastenausgleich) starten (oder erstellen). Ein Iptag wird verwendet, um die einer Ressource zugeordneten Tags zu spezifisch zu verwenden. Iptag kann mithilfe von New-AzPublicIpTag angegeben und als Eingabe über -IpTags übergeben werden.

### Beispiel 4: Erstellen einer neuen öffentlichen IP-Adresse aus einem Präfix
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $dnsPrefix -Location $location
-PublicIpPrefix publicIpPrefix -Sku Standard
```

Mit diesem Befehl wird eine neue öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll. Dieser Ressource wird sofort eine öffentliche IP-Adresse aus dem angegebenen publicIpPrefix zugewiesen.
Diese Option wird nur für die SKU "Standard" und "Static" AllocationMethod unterstützt.

### Beispiel 5: Erstellen einer neuen globalen öffentlichen IP-Adresse
```powershell
$publicIp = New-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName -AllocationMethod Static -DomainNameLabel $domainNameLabel -Location $location -Sku Standard -Tier Global
```

Mit diesem Befehl wird eine neue globale öffentliche IP-Adressressource erstellt. Für "$dnsPrefix.$location.cloudapp.azure.com" wird ein DNS-Eintrag erstellt, der auf die öffentliche IP-Adresse dieser Ressource verweisen soll. Dieser Ressource wird sofort eine globale öffentliche IP-Adresse zugewiesen.
Diese Option wird nur für die SKU "Standard" und "Static" AllocationMethod unterstützt.

## PARAMETERS

### -AllocationMethod
Gibt die Methode an, mit der die öffentliche IP-Adresse zugewiesen werden soll.
Die zulässigen Werte für diesen Parameter sind: Statisch oder dynamisch.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Dynamic, Static

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DomainNameLabel
Gibt den relativen DNS-Namen für eine öffentliche IP-Adresse an.

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

### -Force
Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.

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

### -IdleTimeoutInMinutes
Gibt die Leerlaufzeit in Minuten an.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpAddressVersion
Gibt die Version der IP-Adresse an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
IpTag-Liste.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Gibt die Region an, in der eine öffentliche IP-Adresse erstellt werden soll.

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
Gibt den Namen der öffentlichen IP-Adresse an, die von diesem Cmdlet erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIpPrefix
Gibt den PSPublicIpPrefix an, dem die öffentliche IP-Adresse zugewiesen werden soll.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, in der eine öffentliche IP-Adresse erstellt werden soll.

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

### -ReverseFqdn
Gibt einen umgekehrten vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) an.

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

### -SKU
Der öffentliche IP-SKU-Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Schlüssel-Wert-Paare in Form einer Hashtabelle. Beispiel: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
Die öffentliche IP-SKU-Stufe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugeordnete IP aufgeführt wird, muss stammen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Network.Models.PSPublicIpTag[]

### Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix

### System.Int32

### System.String[]

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPublicIpAddress](./Get-AzPublicIpAddress.md)

[Remove-AzPublicIpAddress](./Remove-AzPublicIpAddress.md)

[Set-AzPublicIpAddress](./Set-AzPublicIpAddress.md)
