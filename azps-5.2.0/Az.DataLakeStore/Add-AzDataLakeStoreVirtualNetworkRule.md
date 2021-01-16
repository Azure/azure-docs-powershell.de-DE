---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297515"
---
# <span data-ttu-id="ea896-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ea896-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ea896-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea896-102">SYNOPSIS</span></span>
<span data-ttu-id="ea896-103">Fügt dem angegebenen Data Lake Store-Konto eine virtuelle Netzwerkregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea896-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ea896-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea896-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea896-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea896-105">DESCRIPTION</span></span>
<span data-ttu-id="ea896-106">Das **Cmdlet "Add-AzDataLakeStoreVirtualNetworkRule"** fügt dem angegebenen Data Lake Store-Konto eine virtuelle Netzwerkregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea896-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="ea896-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea896-107">EXAMPLES</span></span>

### <span data-ttu-id="ea896-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea896-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="ea896-109">Dadurch wird eine neue virtuelle Netzwerkregel namens "myVNET" im Konto "dls" mit der Subnetz-ID "testId" erstellt.</span><span class="sxs-lookup"><span data-stu-id="ea896-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="ea896-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea896-110">PARAMETERS</span></span>

### <span data-ttu-id="ea896-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="ea896-111">-Account</span></span>
<span data-ttu-id="ea896-112">Das Data Lake Store-Konto, dem die virtuelle Netzwerkregel hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="ea896-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="ea896-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea896-113">-DefaultProfile</span></span>
<span data-ttu-id="ea896-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea896-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea896-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ea896-115">-Name</span></span>
<span data-ttu-id="ea896-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ea896-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="ea896-117">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ea896-117">-SubnetId</span></span>
<span data-ttu-id="ea896-118">Die Subnetz-ID der Regel für das virtuelle Netzwerk</span><span class="sxs-lookup"><span data-stu-id="ea896-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="ea896-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea896-119">-Confirm</span></span>
<span data-ttu-id="ea896-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea896-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea896-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ea896-121">-WhatIf</span></span>
<span data-ttu-id="ea896-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea896-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea896-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea896-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea896-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea896-124">CommonParameters</span></span>
<span data-ttu-id="ea896-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea896-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea896-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea896-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea896-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea896-127">INPUTS</span></span>

### <span data-ttu-id="ea896-128">System.String</span><span class="sxs-lookup"><span data-stu-id="ea896-128">System.String</span></span>

## <span data-ttu-id="ea896-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea896-129">OUTPUTS</span></span>

### <span data-ttu-id="ea896-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ea896-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="ea896-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ea896-131">NOTES</span></span>

## <span data-ttu-id="ea896-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ea896-132">RELATED LINKS</span></span>
