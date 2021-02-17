---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164716"
---
# <span data-ttu-id="f53ea-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f53ea-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="f53ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f53ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f53ea-103">Aktualisieren der Eigenschaft "NetworkRule" eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f53ea-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f53ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f53ea-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f53ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f53ea-105">DESCRIPTION</span></span>
<span data-ttu-id="f53ea-106">Das **Cmdlet "Update-AzStorageAccountNetworkRuleSet"** aktualisiert die Eigenschaft "NetworkRule" eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f53ea-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f53ea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f53ea-107">EXAMPLES</span></span>

### <span data-ttu-id="f53ea-108">Beispiel 1: Aktualisieren aller Eigenschaften von NetworkRule, Eingaberegeln mit JSON</span><span class="sxs-lookup"><span data-stu-id="f53ea-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="f53ea-109">Mit diesem Befehl werden alle Eigenschaften von NetworkRule und Eingaberegeln mit JSON aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f53ea-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="f53ea-110">Beispiel 2: Aktualisieren der Umgehungseigenschaft von NetworkRule</span><span class="sxs-lookup"><span data-stu-id="f53ea-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="f53ea-111">Mit diesem Befehl wird die Umgehungseigenschaft von NetworkRule aktualisiert (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="f53ea-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="f53ea-112">Beispiel 3: Bereinigen von Regeln von "NetworkRule" eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f53ea-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="f53ea-113">Mit diesem Befehl werden Die Regeln von "NetworkRule" eines Speicherkontos bereinigt (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="f53ea-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="f53ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f53ea-114">PARAMETERS</span></span>

### <span data-ttu-id="f53ea-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f53ea-115">-AsJob</span></span>
<span data-ttu-id="f53ea-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f53ea-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f53ea-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="f53ea-117">-Bypass</span></span>
<span data-ttu-id="f53ea-118">Der Umgehungswert, der auf die Eigenschaft "NetworkRule" eines Speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f53ea-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="f53ea-119">Der zulässige Wert ist keine oder eine beliebige Kombination aus: • Protokollierung • Metriken • Azureservices</span><span class="sxs-lookup"><span data-stu-id="f53ea-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ea-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="f53ea-120">-DefaultAction</span></span>
<span data-ttu-id="f53ea-121">Der DefaultAction-Wert, der auf die Eigenschaft "NetworkRule" eines Speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f53ea-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="f53ea-122">Die zulässigen Optionen: • Zulassen • Verweigern</span><span class="sxs-lookup"><span data-stu-id="f53ea-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53ea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53ea-123">-DefaultProfile</span></span>
<span data-ttu-id="f53ea-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f53ea-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f53ea-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f53ea-125">-IPRule</span></span>
<span data-ttu-id="f53ea-126">Das Array von IpRule-Objekten, die auf die Eigenschaft "NetworkRule" eines Speicherkontos aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f53ea-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f53ea-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f53ea-127">-Name</span></span>
<span data-ttu-id="f53ea-128">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f53ea-128">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f53ea-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53ea-129">-ResourceGroupName</span></span>
<span data-ttu-id="f53ea-130">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="f53ea-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f53ea-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f53ea-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="f53ea-132">Das Array von VirtualNetworkRule-Objekten, die auf die "NetworkRule"-Eigenschaft eines Speicherkontos aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f53ea-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f53ea-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f53ea-133">-Confirm</span></span>
<span data-ttu-id="f53ea-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f53ea-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f53ea-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f53ea-135">-WhatIf</span></span>
<span data-ttu-id="f53ea-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f53ea-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f53ea-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f53ea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f53ea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53ea-138">CommonParameters</span></span>
<span data-ttu-id="f53ea-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53ea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53ea-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53ea-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53ea-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f53ea-141">INPUTS</span></span>

### <span data-ttu-id="f53ea-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f53ea-142">System.String</span></span>

### <span data-ttu-id="f53ea-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="f53ea-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="f53ea-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="f53ea-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="f53ea-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f53ea-145">OUTPUTS</span></span>

### <span data-ttu-id="f53ea-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f53ea-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="f53ea-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f53ea-147">NOTES</span></span>

## <span data-ttu-id="f53ea-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f53ea-148">RELATED LINKS</span></span>
