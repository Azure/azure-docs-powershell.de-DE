---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: e5b6c552d736571acb484ca301372e9eb32d3944
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946144"
---
# <span data-ttu-id="b4e1a-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b4e1a-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b4e1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e1a-103">Fügt dem angegebenen Data Lake Store-Konto eine Virtuelle Netzwerkregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b4e1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4e1a-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e1a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="b4e1a-106">Das **Add-AzDataLakeStoreVirtualNetworkRule-Cmdlet** fügt dem angegebenen Data Lake Store-Konto eine virtuelle Netzwerkregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="b4e1a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4e1a-107">EXAMPLES</span></span>

### <span data-ttu-id="b4e1a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4e1a-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="b4e1a-109">Dadurch wird eine neue virtuelle Netzwerkregel namens "myVNET" im Konto "dls" mit der Subnetz-ID "testId" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="b4e1a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b4e1a-110">PARAMETERS</span></span>

### <span data-ttu-id="b4e1a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="b4e1a-111">-Account</span></span>
<span data-ttu-id="b4e1a-112">Das Data Lake Store-Konto, dem die Regel für virtuelle Netzwerke hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="b4e1a-112">The Data Lake Store account to add the virtual network rule to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4e1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e1a-113">-DefaultProfile</span></span>
<span data-ttu-id="b4e1a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e1a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b4e1a-115">-Name</span></span>
<span data-ttu-id="b4e1a-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b4e1a-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b4e1a-117">-SubnetId</span></span>
<span data-ttu-id="b4e1a-118">Die Subnetz-Id der Regel für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="b4e1a-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="b4e1a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4e1a-119">-Confirm</span></span>
<span data-ttu-id="b4e1a-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e1a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e1a-121">-WhatIf</span></span>
<span data-ttu-id="b4e1a-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4e1a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e1a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e1a-124">CommonParameters</span></span>
<span data-ttu-id="b4e1a-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e1a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e1a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e1a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e1a-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4e1a-127">INPUTS</span></span>

### <span data-ttu-id="b4e1a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b4e1a-128">System.String</span></span>

## <span data-ttu-id="b4e1a-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4e1a-129">OUTPUTS</span></span>

### <span data-ttu-id="b4e1a-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b4e1a-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="b4e1a-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b4e1a-131">NOTES</span></span>

## <span data-ttu-id="b4e1a-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b4e1a-132">RELATED LINKS</span></span>
