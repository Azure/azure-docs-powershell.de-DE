---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 98f4dd2a1076df1954674f67829e3ee14da1d871
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941208"
---
# <span data-ttu-id="65a2b-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="65a2b-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="65a2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65a2b-102">SYNOPSIS</span></span>
<span data-ttu-id="65a2b-103">Ändert die angegebene Virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="65a2b-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="65a2b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65a2b-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65a2b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65a2b-105">DESCRIPTION</span></span>
<span data-ttu-id="65a2b-106">Das **Cmdlet Set-AzDataLakeStoreVirtualNetworkRule** ändert die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="65a2b-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="65a2b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65a2b-107">EXAMPLES</span></span>

### <span data-ttu-id="65a2b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65a2b-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="65a2b-109">Aktualisiert die Subnetz-ID der Virtuellen Netzwerkregel "myVNET" im Konto "dls" auf "updatedId"</span><span class="sxs-lookup"><span data-stu-id="65a2b-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="65a2b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="65a2b-110">PARAMETERS</span></span>

### <span data-ttu-id="65a2b-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="65a2b-111">-Account</span></span>
<span data-ttu-id="65a2b-112">Das Data Lake Store-Konto zum Aktualisieren der Virtuellen Netzwerkregel in</span><span class="sxs-lookup"><span data-stu-id="65a2b-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="65a2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a2b-113">-DefaultProfile</span></span>
<span data-ttu-id="65a2b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65a2b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65a2b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="65a2b-115">-Name</span></span>
<span data-ttu-id="65a2b-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="65a2b-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="65a2b-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="65a2b-117">-SubnetId</span></span>
<span data-ttu-id="65a2b-118">Der Anfang des gültigen IP-Bereichs für die Regel des virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="65a2b-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="65a2b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65a2b-119">-Confirm</span></span>
<span data-ttu-id="65a2b-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65a2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a2b-121">-WhatIf</span></span>
<span data-ttu-id="65a2b-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65a2b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65a2b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65a2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a2b-124">CommonParameters</span></span>
<span data-ttu-id="65a2b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a2b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a2b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a2b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65a2b-127">INPUTS</span></span>

### <span data-ttu-id="65a2b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="65a2b-128">System.String</span></span>

## <span data-ttu-id="65a2b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65a2b-129">OUTPUTS</span></span>

### <span data-ttu-id="65a2b-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="65a2b-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="65a2b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="65a2b-131">NOTES</span></span>

## <span data-ttu-id="65a2b-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="65a2b-132">RELATED LINKS</span></span>
