---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 64a2963f0b474341480b8e4794370ba90cffd71f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658717"
---
# <span data-ttu-id="58bdd-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="58bdd-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="58bdd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="58bdd-103">Aktualisieren der NetworkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="58bdd-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="58bdd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58bdd-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58bdd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58bdd-105">DESCRIPTION</span></span>
<span data-ttu-id="58bdd-106">Das Cmdlet **Update-AzStorageAccountNetworkRuleSet** aktualisiert die NetworkRule-Eigenschaft eines speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="58bdd-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="58bdd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58bdd-107">EXAMPLES</span></span>

### <span data-ttu-id="58bdd-108">Beispiel 1: Aktualisieren aller Eigenschaften von NetworkRule, eingeben von Regeln mit JSON</span><span class="sxs-lookup"><span data-stu-id="58bdd-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="58bdd-109">Mit diesem Befehl werden alle Eigenschaften von NetworkRule, Eingaberegeln mit JSON, aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="58bdd-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="58bdd-110">Beispiel 2: Update-Bypass-Eigenschaft von NetworkRule</span><span class="sxs-lookup"><span data-stu-id="58bdd-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="58bdd-111">Diese Befehls Update-Bypass-Eigenschaft von NetworkRule (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="58bdd-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="58bdd-112">Beispiel 3: Bereinigen von NetworkRule-Regeln eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="58bdd-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="58bdd-113">Mit diesem Befehl werden Regeln für die NetworkRule eines speicherkontos bereinigt (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="58bdd-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="58bdd-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="58bdd-114">PARAMETERS</span></span>

### <span data-ttu-id="58bdd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58bdd-115">-AsJob</span></span>
<span data-ttu-id="58bdd-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="58bdd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58bdd-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="58bdd-117">-Bypass</span></span>
<span data-ttu-id="58bdd-118">Der Bypass-Wert, der auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="58bdd-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="58bdd-119">Der zulässige Wert ist None oder eine Kombination aus: • Protokollierung • Metriken • Azureservices</span><span class="sxs-lookup"><span data-stu-id="58bdd-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="58bdd-120">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="58bdd-120">-DefaultAction</span></span>
<span data-ttu-id="58bdd-121">Der Standardwert, der auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="58bdd-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="58bdd-122">Zulässige Optionen: • zulassen • ablehnen</span><span class="sxs-lookup"><span data-stu-id="58bdd-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58bdd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bdd-123">-DefaultProfile</span></span>
<span data-ttu-id="58bdd-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="58bdd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58bdd-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="58bdd-125">-IPRule</span></span>
<span data-ttu-id="58bdd-126">Das Array der IpRule-Objekte, die auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="58bdd-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="58bdd-127">-Name</span><span class="sxs-lookup"><span data-stu-id="58bdd-127">-Name</span></span>
<span data-ttu-id="58bdd-128">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="58bdd-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="58bdd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58bdd-129">-ResourceGroupName</span></span>
<span data-ttu-id="58bdd-130">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="58bdd-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="58bdd-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="58bdd-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="58bdd-132">Das Array der VirtualNetworkRule-Objekte, die auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="58bdd-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="58bdd-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="58bdd-133">-Confirm</span></span>
<span data-ttu-id="58bdd-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="58bdd-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58bdd-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58bdd-135">-WhatIf</span></span>
<span data-ttu-id="58bdd-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58bdd-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58bdd-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="58bdd-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58bdd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bdd-138">CommonParameters</span></span>
<span data-ttu-id="58bdd-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58bdd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bdd-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58bdd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bdd-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58bdd-141">INPUTS</span></span>

### <span data-ttu-id="58bdd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="58bdd-142">System.String</span></span>

### <span data-ttu-id="58bdd-143">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="58bdd-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="58bdd-144">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="58bdd-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="58bdd-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58bdd-145">OUTPUTS</span></span>

### <span data-ttu-id="58bdd-146">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="58bdd-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="58bdd-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="58bdd-147">NOTES</span></span>

## <span data-ttu-id="58bdd-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58bdd-148">RELATED LINKS</span></span>
