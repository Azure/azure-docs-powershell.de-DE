---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 546364e96f7beed16ae8786dc3aaacbf9a84454d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926923"
---
# <span data-ttu-id="a7868-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a7868-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="a7868-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7868-102">SYNOPSIS</span></span>
<span data-ttu-id="a7868-103">Ruft Details zu einem Azure NetApp-Dateipool (ANF) ab.</span><span class="sxs-lookup"><span data-stu-id="a7868-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="a7868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7868-104">SYNTAX</span></span>

### <span data-ttu-id="a7868-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7868-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7868-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7868-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7868-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7868-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7868-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7868-108">DESCRIPTION</span></span>
<span data-ttu-id="a7868-109">Das **Get-AzNetAppFilesPool-Cmdlet** ruft Details zu einem ANF-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="a7868-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="a7868-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7868-110">EXAMPLES</span></span>

### <span data-ttu-id="a7868-111">Beispiel 1: Erhalten eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="a7868-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="a7868-112">Dieser Befehl ruft das Konto "MyAnfPool" aus dem Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="a7868-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="a7868-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7868-113">PARAMETERS</span></span>

### <span data-ttu-id="a7868-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a7868-114">-AccountName</span></span>
<span data-ttu-id="a7868-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="a7868-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7868-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a7868-116">-AccountObject</span></span>
<span data-ttu-id="a7868-117">Das Kontoobjekt, das den zurückzukehrenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="a7868-117">The account object containing the pool to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7868-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7868-118">-DefaultProfile</span></span>
<span data-ttu-id="a7868-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7868-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7868-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a7868-120">-Name</span></span>
<span data-ttu-id="a7868-121">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="a7868-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7868-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7868-122">-ResourceGroupName</span></span>
<span data-ttu-id="a7868-123">Die Ressourcengruppe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="a7868-123">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7868-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7868-124">-ResourceId</span></span>
<span data-ttu-id="a7868-125">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="a7868-125">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7868-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7868-126">CommonParameters</span></span>
<span data-ttu-id="a7868-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7868-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7868-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7868-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7868-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7868-129">INPUTS</span></span>

### <span data-ttu-id="a7868-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a7868-130">System.String</span></span>

### <span data-ttu-id="a7868-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a7868-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a7868-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7868-132">OUTPUTS</span></span>

### <span data-ttu-id="a7868-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a7868-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a7868-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7868-134">NOTES</span></span>

## <span data-ttu-id="a7868-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7868-135">RELATED LINKS</span></span>
