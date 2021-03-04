---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: ec5ac8ab949b95fba3f82ea795dadcecfac360ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931184"
---
# <span data-ttu-id="3f848-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f848-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="3f848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f848-102">SYNOPSIS</span></span>
<span data-ttu-id="3f848-103">Ruft die angegebenen Regeln für virtuelle Netzwerke im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="3f848-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="3f848-104">Wenn keine Regel für virtuelle Netzwerke angegeben ist, werden alle Regeln für das virtuelle Netzwerk für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f848-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="3f848-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f848-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f848-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f848-106">DESCRIPTION</span></span>
<span data-ttu-id="3f848-107">Das Get-AzDataLakeStoreVirtualNetworkRule-Cmdlet ruft die angegebenen Regeln für virtuelle Netzwerke im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="3f848-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="3f848-108">Wenn keine Regel für virtuelle Netzwerke angegeben ist, werden alle Regeln für das virtuelle Netzwerk für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f848-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="3f848-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f848-109">EXAMPLES</span></span>

### <span data-ttu-id="3f848-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f848-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="3f848-111">Gibt die Virtuelle Netzwerkregel mit dem Namen "myVNET" von Konto "dls" zurück.</span><span class="sxs-lookup"><span data-stu-id="3f848-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="3f848-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f848-112">PARAMETERS</span></span>

### <span data-ttu-id="3f848-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="3f848-113">-Account</span></span>
<span data-ttu-id="3f848-114">Das Data Lake Store-Konto, aus dem die Regel für virtuelle Netzwerke</span><span class="sxs-lookup"><span data-stu-id="3f848-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="3f848-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f848-115">-DefaultProfile</span></span>
<span data-ttu-id="3f848-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f848-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f848-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3f848-117">-Name</span></span>
<span data-ttu-id="3f848-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="3f848-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="3f848-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f848-119">CommonParameters</span></span>
<span data-ttu-id="3f848-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f848-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f848-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f848-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f848-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f848-122">INPUTS</span></span>

### <span data-ttu-id="3f848-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3f848-123">System.String</span></span>

## <span data-ttu-id="3f848-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f848-124">OUTPUTS</span></span>

### <span data-ttu-id="3f848-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f848-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="3f848-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f848-126">NOTES</span></span>

## <span data-ttu-id="3f848-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f848-127">RELATED LINKS</span></span>
