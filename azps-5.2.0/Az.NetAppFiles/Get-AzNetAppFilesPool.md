---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: d41ce912761770d724fd700249f07d0af11c9647
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360070"
---
# <span data-ttu-id="0164b-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0164b-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="0164b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0164b-102">SYNOPSIS</span></span>
<span data-ttu-id="0164b-103">Ruft Details zu einem Azure NetApp Files (ANF)-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="0164b-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="0164b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0164b-104">SYNTAX</span></span>

### <span data-ttu-id="0164b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0164b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0164b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0164b-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0164b-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0164b-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0164b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0164b-108">DESCRIPTION</span></span>
<span data-ttu-id="0164b-109">Das **Cmdlet "Get-AzNetAppFilesPool"** ruft Details zu einem ANF-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="0164b-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="0164b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0164b-110">EXAMPLES</span></span>

### <span data-ttu-id="0164b-111">Beispiel 1: Erhalten eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="0164b-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="0164b-112">Dieser Befehl ruft das Konto mit dem Namen "MyAnfPool" aus dem Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="0164b-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="0164b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0164b-113">PARAMETERS</span></span>

### <span data-ttu-id="0164b-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0164b-114">-AccountName</span></span>
<span data-ttu-id="0164b-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="0164b-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="0164b-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="0164b-116">-AccountObject</span></span>
<span data-ttu-id="0164b-117">Das Kontoobjekt, das den zurückzukehrenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="0164b-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="0164b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0164b-118">-DefaultProfile</span></span>
<span data-ttu-id="0164b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0164b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0164b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0164b-120">-Name</span></span>
<span data-ttu-id="0164b-121">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="0164b-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="0164b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0164b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0164b-123">Die Ressourcengruppe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="0164b-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="0164b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0164b-124">-ResourceId</span></span>
<span data-ttu-id="0164b-125">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="0164b-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="0164b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0164b-126">CommonParameters</span></span>
<span data-ttu-id="0164b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0164b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0164b-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0164b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0164b-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0164b-129">INPUTS</span></span>

### <span data-ttu-id="0164b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0164b-130">System.String</span></span>

### <span data-ttu-id="0164b-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="0164b-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="0164b-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0164b-132">OUTPUTS</span></span>

### <span data-ttu-id="0164b-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="0164b-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="0164b-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0164b-134">NOTES</span></span>

## <span data-ttu-id="0164b-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0164b-135">RELATED LINKS</span></span>
