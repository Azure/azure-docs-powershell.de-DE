---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 03e6169a9e69b9f2faa3dfaccba934428f7db4e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929259"
---
# <span data-ttu-id="940f8-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="940f8-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="940f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="940f8-102">SYNOPSIS</span></span>
<span data-ttu-id="940f8-103">Aktualisieren der NetworkRule-Eigenschaft eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="940f8-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="940f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="940f8-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-ResourceAccessRule <PSResourceAccessRule[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="940f8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="940f8-105">DESCRIPTION</span></span>
<span data-ttu-id="940f8-106">Das **Cmdlet Update-AzStorageAccountNetworkRuleSet** aktualisiert die NetworkRule-Eigenschaft eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="940f8-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="940f8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="940f8-107">EXAMPLES</span></span>

### <span data-ttu-id="940f8-108">Beispiel 1: Aktualisieren aller Eigenschaften von NetworkRule, Eingaberegeln mit JSON</span><span class="sxs-lookup"><span data-stu-id="940f8-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"}) -ResourceAccessRule (@{ResourceId=$ResourceId1;TenantId=$tenantId1},@{ResourceId=$ResourceId2;TenantId=$tenantId1})
```

<span data-ttu-id="940f8-109">Dieser Befehl aktualisiert alle Eigenschaften von NetworkRule, Eingaberegeln mit JSON.</span><span class="sxs-lookup"><span data-stu-id="940f8-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="940f8-110">Beispiel 2: Update Bypass-Eigenschaft von NetworkRule</span><span class="sxs-lookup"><span data-stu-id="940f8-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="940f8-111">Dieses Befehlsupdate Umgehen der Eigenschaft von NetworkRule (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="940f8-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="940f8-112">Beispiel 3: Bereinigen von Regeln für NetworkRule eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="940f8-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @() -ResourceAccessRule @()
```

<span data-ttu-id="940f8-113">Mit diesem Befehl werden Regeln von NetworkRule eines Speicherkontos bereinigt (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="940f8-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="940f8-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="940f8-114">PARAMETERS</span></span>

### <span data-ttu-id="940f8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="940f8-115">-AsJob</span></span>
<span data-ttu-id="940f8-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="940f8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="940f8-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="940f8-117">-Bypass</span></span>
<span data-ttu-id="940f8-118">Der Wert umgehen, der auf die NetworkRule-Eigenschaft eines Speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="940f8-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="940f8-119">Der zulässige Wert ist keine oder eine beliebige Kombination aus: • Protokollierung • Metriken • Azureservices</span><span class="sxs-lookup"><span data-stu-id="940f8-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="940f8-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="940f8-120">-DefaultAction</span></span>
<span data-ttu-id="940f8-121">Der Standardwert, der auf die NetworkRule-Eigenschaft eines Speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="940f8-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="940f8-122">Die zulässigen Optionen: • Zulassen • Verweigern</span><span class="sxs-lookup"><span data-stu-id="940f8-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="940f8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="940f8-123">-DefaultProfile</span></span>
<span data-ttu-id="940f8-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="940f8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="940f8-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="940f8-125">-IPRule</span></span>
<span data-ttu-id="940f8-126">Das Array der IpRule-Objekte, die auf die NetworkRule-Eigenschaft eines Speicherkontos aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="940f8-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="940f8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="940f8-127">-Name</span></span>
<span data-ttu-id="940f8-128">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="940f8-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="940f8-129">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="940f8-129">-ResourceAccessRule</span></span>
<span data-ttu-id="940f8-130">Storage Account NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="940f8-130">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="940f8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="940f8-131">-ResourceGroupName</span></span>
<span data-ttu-id="940f8-132">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="940f8-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="940f8-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="940f8-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="940f8-134">Das Array von VirtualNetworkRule-Objekten, die auf die NetworkRule-Eigenschaft eines Speicherkontos aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="940f8-134">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="940f8-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="940f8-135">-Confirm</span></span>
<span data-ttu-id="940f8-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="940f8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="940f8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="940f8-137">-WhatIf</span></span>
<span data-ttu-id="940f8-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="940f8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="940f8-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="940f8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="940f8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940f8-140">CommonParameters</span></span>
<span data-ttu-id="940f8-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="940f8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940f8-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940f8-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940f8-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="940f8-143">INPUTS</span></span>

### <span data-ttu-id="940f8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="940f8-144">System.String</span></span>

### <span data-ttu-id="940f8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="940f8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="940f8-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="940f8-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="940f8-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="940f8-147">OUTPUTS</span></span>

### <span data-ttu-id="940f8-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="940f8-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="940f8-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="940f8-149">NOTES</span></span>

## <span data-ttu-id="940f8-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="940f8-150">RELATED LINKS</span></span>
