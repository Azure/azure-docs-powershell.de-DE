---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 61c5fc7f80ab157724156d86a5cbb8df8bb23841
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650431"
---
# <span data-ttu-id="4bc10-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bc10-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="4bc10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bc10-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc10-103">Erstellt einen neuen Analysis Services-Server</span><span class="sxs-lookup"><span data-stu-id="4bc10-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="4bc10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bc10-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bc10-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bc10-105">DESCRIPTION</span></span>
<span data-ttu-id="4bc10-106">Das New-AzAnalysisServicesServer-Cmdlet erstellt einen neuen Analysis Services-Server.</span><span class="sxs-lookup"><span data-stu-id="4bc10-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="4bc10-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bc10-107">EXAMPLES</span></span>

### <span data-ttu-id="4bc10-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4bc10-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="4bc10-109">Erstellt einen Server mit dem Namen Testserver im Azure Region West-US und in der Ressourcengruppe testresrourcegroup.</span><span class="sxs-lookup"><span data-stu-id="4bc10-109">Creates a server named testserver in the Azure region West-US and in resource group testresrourcegroup.</span></span> <span data-ttu-id="4bc10-110">Die SKU-Ebene für den Server ist S1.</span><span class="sxs-lookup"><span data-stu-id="4bc10-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="4bc10-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bc10-111">PARAMETERS</span></span>

### <span data-ttu-id="4bc10-112">– Administrator</span><span class="sxs-lookup"><span data-stu-id="4bc10-112">-Administrator</span></span>
<span data-ttu-id="4bc10-113">Eine Zeichenfolge, die eine durch Kommas getrennte Liste der Benutzer oder Gruppen darstellt, die als Administratoren auf dem Server eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4bc10-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="4bc10-114">Die Benutzer oder Gruppen müssen als UPN-Format angegeben werden, beispielsweise user@contoso.com oder groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="4bc10-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="4bc10-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="4bc10-116">Der BLOB-Container-URI für die Sicherung des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="4bc10-116">The blob container Uri for backup the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="4bc10-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="4bc10-118">Standardverbindungsmodus eines Analysis Service-Servers</span><span class="sxs-lookup"><span data-stu-id="4bc10-118">Default connection mode of an Analysis service server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc10-119">-DefaultProfile</span></span>
<span data-ttu-id="4bc10-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4bc10-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bc10-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="4bc10-121">-FirewallConfig</span></span>
<span data-ttu-id="4bc10-122">Firewall-Konfiguration eines Analysis-Servers</span><span class="sxs-lookup"><span data-stu-id="4bc10-122">Firewall config of an Analysis server</span></span>

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4bc10-123">-GatewayResourceId</span></span>
<span data-ttu-id="4bc10-124">Gateway-Ressourcen-ID für assocaite zu einem Analysis-Server</span><span class="sxs-lookup"><span data-stu-id="4bc10-124">Gateway resource Id for assocaite to an Analysis server</span></span>

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

### <span data-ttu-id="4bc10-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="4bc10-125">-Location</span></span>
<span data-ttu-id="4bc10-126">Der Azure-Bereich, in dem der Analysis Services-Server gehostet wird</span><span class="sxs-lookup"><span data-stu-id="4bc10-126">The Azure region where the Analysis Services server is hosted</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4bc10-127">-Name</span></span>
<span data-ttu-id="4bc10-128">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="4bc10-128">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="4bc10-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="4bc10-130">Anzahl der Replikate eines Analysis-Service-Servers nur lesen</span><span class="sxs-lookup"><span data-stu-id="4bc10-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="4bc10-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc10-131">-ResourceGroupName</span></span>
<span data-ttu-id="4bc10-132">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="4bc10-132">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="4bc10-133">-Sku</span></span>
<span data-ttu-id="4bc10-134">Der Name der SKU für den Server.</span><span class="sxs-lookup"><span data-stu-id="4bc10-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="4bc10-135">Die unterstützten Werte sind 0 ', ist 1 ', ist 2 ', ist 4 ' für die Standard Ebene; "B1", "B2" für die grundlegende Ebene und 'd 1 für die Entwicklungsstufe.</span><span class="sxs-lookup"><span data-stu-id="4bc10-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="4bc10-136">-Tag</span></span>
<span data-ttu-id="4bc10-137">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="4bc10-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc10-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bc10-138">-Confirm</span></span>
<span data-ttu-id="4bc10-139">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="4bc10-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="4bc10-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc10-140">-WhatIf</span></span>
<span data-ttu-id="4bc10-141">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="4bc10-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="4bc10-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc10-142">CommonParameters</span></span>
<span data-ttu-id="4bc10-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bc10-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc10-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bc10-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc10-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bc10-145">INPUTS</span></span>

### <span data-ttu-id="4bc10-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4bc10-146">System.String</span></span>

### <span data-ttu-id="4bc10-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4bc10-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="4bc10-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4bc10-148">System.Int32</span></span>

### <span data-ttu-id="4bc10-149">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="4bc10-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="4bc10-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bc10-150">OUTPUTS</span></span>

### <span data-ttu-id="4bc10-151">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bc10-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="4bc10-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bc10-152">NOTES</span></span>
<span data-ttu-id="4bc10-153">Alias: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="4bc10-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="4bc10-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bc10-154">RELATED LINKS</span></span>

[<span data-ttu-id="4bc10-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bc10-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="4bc10-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4bc10-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
