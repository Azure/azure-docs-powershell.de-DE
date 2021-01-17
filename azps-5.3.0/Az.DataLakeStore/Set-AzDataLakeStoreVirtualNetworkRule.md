---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 1c649a63e8ba57a3d2e9f9af28e0ce4b12ca9a0d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458030"
---
# <span data-ttu-id="1ba46-101">Set-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1ba46-101">Set-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="1ba46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ba46-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba46-103">Ändert die angegebene Virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ba46-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1ba46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ba46-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba46-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ba46-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba46-106">Das **Cmdlet "Set-AzDataLakeStoreVirtualNetworkRule"** ändert die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1ba46-106">The **Set-AzDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="1ba46-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1ba46-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba46-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1ba46-108">Example 1</span></span>
```powershell
PS C:\> Set-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="1ba46-109">Aktualisiert die Subnetz-ID der virtuellen Netzwerkregel "myVNET" im Konto "dls" auf "updatedId".</span><span class="sxs-lookup"><span data-stu-id="1ba46-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="1ba46-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ba46-110">PARAMETERS</span></span>

### <span data-ttu-id="1ba46-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1ba46-111">-Account</span></span>
<span data-ttu-id="1ba46-112">Das Data Lake Store-Konto zum Aktualisieren der virtuellen Netzwerkregel in</span><span class="sxs-lookup"><span data-stu-id="1ba46-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="1ba46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba46-113">-DefaultProfile</span></span>
<span data-ttu-id="1ba46-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ba46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ba46-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1ba46-115">-Name</span></span>
<span data-ttu-id="1ba46-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1ba46-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="1ba46-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1ba46-117">-SubnetId</span></span>
<span data-ttu-id="1ba46-118">Start des gültigen IP-Bereichs für die virtuelle Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="1ba46-118">The start of the valid ip range for the virtual network rule</span></span>

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

### <span data-ttu-id="1ba46-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ba46-119">-Confirm</span></span>
<span data-ttu-id="1ba46-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ba46-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba46-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1ba46-121">-WhatIf</span></span>
<span data-ttu-id="1ba46-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ba46-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba46-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ba46-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba46-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba46-124">CommonParameters</span></span>
<span data-ttu-id="1ba46-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ba46-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba46-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ba46-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba46-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1ba46-127">INPUTS</span></span>

### <span data-ttu-id="1ba46-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1ba46-128">System.String</span></span>

## <span data-ttu-id="1ba46-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1ba46-129">OUTPUTS</span></span>

### <span data-ttu-id="1ba46-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1ba46-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="1ba46-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1ba46-131">NOTES</span></span>

## <span data-ttu-id="1ba46-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1ba46-132">RELATED LINKS</span></span>
