---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 7e6b41a081b5170a34863ff29bf26431224490fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996674"
---
# <span data-ttu-id="6ae91-101">New-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6ae91-101">New-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="6ae91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ae91-102">SYNOPSIS</span></span>
<span data-ttu-id="6ae91-103">Erstellt einen neuen Analysis Services-Server</span><span class="sxs-lookup"><span data-stu-id="6ae91-103">Creates a new Analysis Services server</span></span>

## <span data-ttu-id="6ae91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ae91-104">SYNTAX</span></span>

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ae91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ae91-105">DESCRIPTION</span></span>
<span data-ttu-id="6ae91-106">Das New-AzAnalysisServicesServer-Cmdlet erstellt einen neuen Analysis Services-Server.</span><span class="sxs-lookup"><span data-stu-id="6ae91-106">The New-AzAnalysisServicesServer cmdlet creates a new Analysis Services server</span></span>

## <span data-ttu-id="6ae91-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ae91-107">EXAMPLES</span></span>

### <span data-ttu-id="6ae91-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6ae91-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

<span data-ttu-id="6ae91-109">Erstellt einen Server mit dem Namen Testserver im Azure Region West-US und in der Ressourcengruppe testresourcegroup.</span><span class="sxs-lookup"><span data-stu-id="6ae91-109">Creates a server named testserver in the Azure region West-US and in resource group testresourcegroup.</span></span> <span data-ttu-id="6ae91-110">Die SKU-Ebene für den Server ist S1.</span><span class="sxs-lookup"><span data-stu-id="6ae91-110">The sku level for the server will be S1.</span></span>

## <span data-ttu-id="6ae91-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ae91-111">PARAMETERS</span></span>

### <span data-ttu-id="6ae91-112">– Administrator</span><span class="sxs-lookup"><span data-stu-id="6ae91-112">-Administrator</span></span>
<span data-ttu-id="6ae91-113">Eine Zeichenfolge, die eine durch Kommas getrennte Liste der Benutzer oder Gruppen darstellt, die als Administratoren auf dem Server eingerichtet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ae91-113">A string representing a comma separated list of users or groups to be set as administrators on the server.</span></span> <span data-ttu-id="6ae91-114">Die Benutzer oder Gruppen müssen als UPN-Format angegeben werden, beispielsweise user@contoso.com oder groups@contoso.com</span><span class="sxs-lookup"><span data-stu-id="6ae91-114">The users or groups need to be specified UPN format e.g. user@contoso.com or groups@contoso.com</span></span>

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

### <span data-ttu-id="6ae91-115">-BackupBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="6ae91-115">-BackupBlobContainerUri</span></span>
<span data-ttu-id="6ae91-116">Der BLOB-Container-URI für die Sicherung des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="6ae91-116">The blob container Uri for backup the Analysis Services server</span></span>

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

### <span data-ttu-id="6ae91-117">-DefaultConnectionMode</span><span class="sxs-lookup"><span data-stu-id="6ae91-117">-DefaultConnectionMode</span></span>
<span data-ttu-id="6ae91-118">Standardverbindungsmodus eines Analysis Service-Servers</span><span class="sxs-lookup"><span data-stu-id="6ae91-118">Default connection mode of an Analysis service server</span></span>

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

### <span data-ttu-id="6ae91-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ae91-119">-DefaultProfile</span></span>
<span data-ttu-id="6ae91-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ae91-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ae91-121">-FirewallConfig</span><span class="sxs-lookup"><span data-stu-id="6ae91-121">-FirewallConfig</span></span>
<span data-ttu-id="6ae91-122">Firewall-Konfiguration eines Analysis-Servers</span><span class="sxs-lookup"><span data-stu-id="6ae91-122">Firewall config of an Analysis server</span></span>

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

### <span data-ttu-id="6ae91-123">-GatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6ae91-123">-GatewayResourceId</span></span>
<span data-ttu-id="6ae91-124">Gateway-Ressourcen-ID, die einem Analysis-Server zugeordnet werden soll</span><span class="sxs-lookup"><span data-stu-id="6ae91-124">Gateway resource Id to associate to an Analysis server</span></span>

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

### <span data-ttu-id="6ae91-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="6ae91-125">-Location</span></span>
<span data-ttu-id="6ae91-126">Der Azure-Bereich, in dem der Analysis Services-Server gehostet wird</span><span class="sxs-lookup"><span data-stu-id="6ae91-126">The Azure region where the Analysis Services server is hosted</span></span>

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

### <span data-ttu-id="6ae91-127">-Name</span><span class="sxs-lookup"><span data-stu-id="6ae91-127">-Name</span></span>
<span data-ttu-id="6ae91-128">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="6ae91-128">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="6ae91-129">-ReadonlyReplicaCount</span><span class="sxs-lookup"><span data-stu-id="6ae91-129">-ReadonlyReplicaCount</span></span>
<span data-ttu-id="6ae91-130">Anzahl der Replikate eines Analysis-Service-Servers nur lesen</span><span class="sxs-lookup"><span data-stu-id="6ae91-130">Read only replica count of an Analysis service server</span></span>

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

### <span data-ttu-id="6ae91-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ae91-131">-ResourceGroupName</span></span>
<span data-ttu-id="6ae91-132">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="6ae91-132">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="6ae91-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="6ae91-133">-Sku</span></span>
<span data-ttu-id="6ae91-134">Der Name der SKU für den Server.</span><span class="sxs-lookup"><span data-stu-id="6ae91-134">The name of the Sku for the server.</span></span>
<span data-ttu-id="6ae91-135">Die unterstützten Werte sind 0 ', ist 1 ', ist 2 ', ist 4 ' für die Standard Ebene; "B1", "B2" für die grundlegende Ebene und 'd 1 für die Entwicklungsstufe.</span><span class="sxs-lookup"><span data-stu-id="6ae91-135">The supported values are 'S0', 'S1', 'S2', 'S4' for the Standard tier; 'B1', 'B2' for the Basic tier and 'D1' for Development tier.</span></span>

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

### <span data-ttu-id="6ae91-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ae91-136">-Tag</span></span>
<span data-ttu-id="6ae91-137">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ae91-137">Key-value pairs in the form of a hash table set as tags on the server.</span></span>

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

### <span data-ttu-id="6ae91-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ae91-138">-Confirm</span></span>
<span data-ttu-id="6ae91-139">Fordert den Benutzer auf, zu bestätigen, dass der Vorgang ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="6ae91-139">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="6ae91-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ae91-140">-WhatIf</span></span>
<span data-ttu-id="6ae91-141">Beschreibt die Aktionen, die vom aktuellen Vorgang ausgeführt werden, ohne diese tatsächlich auszuführen</span><span class="sxs-lookup"><span data-stu-id="6ae91-141">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="6ae91-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ae91-142">CommonParameters</span></span>
<span data-ttu-id="6ae91-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ae91-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ae91-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ae91-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ae91-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ae91-145">INPUTS</span></span>

### <span data-ttu-id="6ae91-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6ae91-146">System.String</span></span>

### <span data-ttu-id="6ae91-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ae91-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6ae91-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6ae91-148">System.Int32</span></span>

### <span data-ttu-id="6ae91-149">Microsoft. Azure. Commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="6ae91-149">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="6ae91-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ae91-150">OUTPUTS</span></span>

### <span data-ttu-id="6ae91-151">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6ae91-151">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="6ae91-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ae91-152">NOTES</span></span>
<span data-ttu-id="6ae91-153">Alias: New-AzAs</span><span class="sxs-lookup"><span data-stu-id="6ae91-153">Alias: New-AzAs</span></span>

## <span data-ttu-id="6ae91-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ae91-154">RELATED LINKS</span></span>

[<span data-ttu-id="6ae91-155">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6ae91-155">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="6ae91-156">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6ae91-156">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
