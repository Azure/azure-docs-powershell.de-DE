---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458073"
---
# <span data-ttu-id="adf8a-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="adf8a-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="adf8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adf8a-102">SYNOPSIS</span></span>
<span data-ttu-id="adf8a-103">Ruft die angegebenen Virtuellen Netzwerkregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="adf8a-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="adf8a-104">Wenn keine Regel für das virtuelle Netzwerk angegeben ist, werden alle Regeln für das virtuelle Netzwerk für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="adf8a-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="adf8a-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="adf8a-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adf8a-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adf8a-106">DESCRIPTION</span></span>
<span data-ttu-id="adf8a-107">Das Get-AzDataLakeStoreVirtualNetworkRule cmdlet ruft die angegebenen virtuellen Netzwerkregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="adf8a-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="adf8a-108">Wenn keine Regel für das virtuelle Netzwerk angegeben ist, werden alle Regeln für das virtuelle Netzwerk für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="adf8a-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="adf8a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="adf8a-109">EXAMPLES</span></span>

### <span data-ttu-id="adf8a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="adf8a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="adf8a-111">Gibt die Virtuelle Netzwerkregel mit dem Namen "myVNET" aus dem Konto "dls" zurück.</span><span class="sxs-lookup"><span data-stu-id="adf8a-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="adf8a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adf8a-112">PARAMETERS</span></span>

### <span data-ttu-id="adf8a-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="adf8a-113">-Account</span></span>
<span data-ttu-id="adf8a-114">Das Data Lake Store-Konto, über das die Regel für das virtuelle Netzwerk</span><span class="sxs-lookup"><span data-stu-id="adf8a-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="adf8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf8a-115">-DefaultProfile</span></span>
<span data-ttu-id="adf8a-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="adf8a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adf8a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="adf8a-117">-Name</span></span>
<span data-ttu-id="adf8a-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="adf8a-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="adf8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf8a-119">CommonParameters</span></span>
<span data-ttu-id="adf8a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adf8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf8a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf8a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf8a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="adf8a-122">INPUTS</span></span>

### <span data-ttu-id="adf8a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="adf8a-123">System.String</span></span>

## <span data-ttu-id="adf8a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="adf8a-124">OUTPUTS</span></span>

### <span data-ttu-id="adf8a-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="adf8a-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="adf8a-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="adf8a-126">NOTES</span></span>

## <span data-ttu-id="adf8a-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="adf8a-127">RELATED LINKS</span></span>
