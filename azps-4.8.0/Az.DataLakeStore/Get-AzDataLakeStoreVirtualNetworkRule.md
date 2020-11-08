---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 95e18d7e36122ed199b4a4c880b4fc918f1164f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165827"
---
# <span data-ttu-id="c9ae5-101">Get-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c9ae5-101">Get-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c9ae5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ae5-103">Ruft die angegebenen virtuellen Netzwerkregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-103">Gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="c9ae5-104">Wenn keine Regel für virtuelles Netzwerk angegeben ist, werden alle virtuellen Netzwerkregeln für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-104">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="c9ae5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9ae5-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ae5-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9ae5-106">DESCRIPTION</span></span>
<span data-ttu-id="c9ae5-107">Das Get-AzDataLakeStoreVirtualNetworkRule-Cmdlet ruft die angegebenen virtuellen Netzwerkregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-107">The Get-AzDataLakeStoreVirtualNetworkRule cmdlet gets the specified virtual network rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="c9ae5-108">Wenn keine Regel für virtuelles Netzwerk angegeben ist, werden alle virtuellen Netzwerkregeln für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-108">If no virtual network rule is specified, then lists all virtual network rules for the account.</span></span>

## <span data-ttu-id="c9ae5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9ae5-109">EXAMPLES</span></span>

### <span data-ttu-id="c9ae5-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c9ae5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="c9ae5-111">Gibt die virtuelle Netzwerkregel mit dem Namen "myVNET" aus dem Konto "DLS" zurück.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-111">Returns the virtual network rule named "myVNET" from account "dls"</span></span>

## <span data-ttu-id="c9ae5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9ae5-112">PARAMETERS</span></span>

### <span data-ttu-id="c9ae5-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="c9ae5-113">-Account</span></span>
<span data-ttu-id="c9ae5-114">Das Data Lake Store-Konto zum Abrufen der Regel für das virtuelle Netzwerk</span><span class="sxs-lookup"><span data-stu-id="c9ae5-114">The Data Lake Store account to get the virtual network rule from</span></span>

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

### <span data-ttu-id="c9ae5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ae5-115">-DefaultProfile</span></span>
<span data-ttu-id="c9ae5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9ae5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c9ae5-117">-Name</span></span>
<span data-ttu-id="c9ae5-118">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="c9ae5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ae5-119">CommonParameters</span></span>
<span data-ttu-id="c9ae5-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ae5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ae5-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ae5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ae5-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9ae5-122">INPUTS</span></span>

### <span data-ttu-id="c9ae5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c9ae5-123">System.String</span></span>

## <span data-ttu-id="c9ae5-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9ae5-124">OUTPUTS</span></span>

### <span data-ttu-id="c9ae5-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c9ae5-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="c9ae5-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9ae5-126">NOTES</span></span>

## <span data-ttu-id="c9ae5-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9ae5-127">RELATED LINKS</span></span>
