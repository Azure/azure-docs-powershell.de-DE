---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664407"
---
# <span data-ttu-id="f0041-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0041-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="f0041-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0041-102">SYNOPSIS</span></span>
<span data-ttu-id="f0041-103">Aktualisieren der NetworkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f0041-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0041-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0041-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0041-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0041-105">DESCRIPTION</span></span>
<span data-ttu-id="f0041-106">Das Cmdlet **Update-AzureRmStorageAccountNetworkRuleSet** aktualisiert die NetworkRule-Eigenschaft eines speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="f0041-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="f0041-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0041-107">EXAMPLES</span></span>

### <span data-ttu-id="f0041-108">Beispiel 1: Aktualisieren aller Eigenschaften von NetworkRule, eingeben von Regeln mit JSON</span><span class="sxs-lookup"><span data-stu-id="f0041-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="f0041-109">Mit diesem Befehl werden alle Eigenschaften von NetworkRule, Eingaberegeln mit JSON, aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f0041-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="f0041-110">Beispiel 2: Update-Bypass-Eigenschaft von NetworkRule</span><span class="sxs-lookup"><span data-stu-id="f0041-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="f0041-111">Diese Befehls Update-Bypass-Eigenschaft von NetworkRule (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="f0041-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="f0041-112">Beispiel 3: Bereinigen von NetworkRule-Regeln eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f0041-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="f0041-113">Mit diesem Befehl werden Regeln für die NetworkRule eines speicherkontos bereinigt (andere Eigenschaften werden nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="f0041-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="f0041-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0041-114">PARAMETERS</span></span>

### <span data-ttu-id="f0041-115">-Bypass</span><span class="sxs-lookup"><span data-stu-id="f0041-115">-Bypass</span></span>
<span data-ttu-id="f0041-116">Der Bypass-Wert, der auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0041-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="f0041-117">Der zulässige Wert ist None oder eine Kombination aus: â € ¢ Protokollierung â € ¢ Metriken â € ¢ Azureservices</span><span class="sxs-lookup"><span data-stu-id="f0041-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

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

### <span data-ttu-id="f0041-118">– Standardmäßig</span><span class="sxs-lookup"><span data-stu-id="f0041-118">-DefaultAction</span></span>
<span data-ttu-id="f0041-119">Der Standardwert, der auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0041-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="f0041-120">Die zulässigen Optionen: â € ¢ Allow â € ¢ verweigern</span><span class="sxs-lookup"><span data-stu-id="f0041-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

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

### <span data-ttu-id="f0041-121">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f0041-121">-IPRule</span></span>
<span data-ttu-id="f0041-122">Das Array der IpRule-Objekte, die auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0041-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="f0041-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f0041-123">-Name</span></span>
<span data-ttu-id="f0041-124">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f0041-124">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="f0041-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0041-125">-ResourceGroupName</span></span>
<span data-ttu-id="f0041-126">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="f0041-126">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f0041-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f0041-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="f0041-128">Das Array der VirtualNetworkRule-Objekte, die auf die NetworkRule-Eigenschaft eines speicherkontos aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0041-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="f0041-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0041-129">-Confirm</span></span>
<span data-ttu-id="f0041-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0041-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0041-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0041-131">-WhatIf</span></span>
<span data-ttu-id="f0041-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0041-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0041-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0041-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0041-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0041-134">-DefaultProfile</span></span>
<span data-ttu-id="f0041-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0041-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0041-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0041-136">CommonParameters</span></span>
<span data-ttu-id="f0041-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0041-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0041-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0041-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0041-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0041-139">INPUTS</span></span>

### <span data-ttu-id="f0041-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f0041-140">System.String</span></span>
<span data-ttu-id="f0041-141">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="f0041-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="f0041-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0041-142">OUTPUTS</span></span>

### <span data-ttu-id="f0041-143">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0041-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="f0041-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0041-144">NOTES</span></span>

## <span data-ttu-id="f0041-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0041-145">RELATED LINKS</span></span>

