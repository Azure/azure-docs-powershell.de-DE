---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: a730bb71ebd6f06bdae4bcbf608987a929a433c3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845223"
---
# <span data-ttu-id="a5049-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a5049-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a5049-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5049-102">SYNOPSIS</span></span>
<span data-ttu-id="a5049-103">Ruft Details eines Azure NetApp-Dateien (ANF)-Volumes ab.</span><span class="sxs-lookup"><span data-stu-id="a5049-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="a5049-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5049-104">SYNTAX</span></span>

### <span data-ttu-id="a5049-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5049-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5049-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5049-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5049-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5049-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5049-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5049-108">DESCRIPTION</span></span>
<span data-ttu-id="a5049-109">Das Cmdlet " **Get-AzNetAppFilesVolume** " ruft Details eines ANF-Volumes ab.</span><span class="sxs-lookup"><span data-stu-id="a5049-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="a5049-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5049-110">EXAMPLES</span></span>

### <span data-ttu-id="a5049-111">Beispiel 1: Abrufen eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="a5049-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="a5049-112">Dieser Befehl ruft das Volume mit dem Namen MyAnfVolume aus dem Pool "MyAnfPool" ab.</span><span class="sxs-lookup"><span data-stu-id="a5049-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="a5049-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5049-113">PARAMETERS</span></span>

### <span data-ttu-id="a5049-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a5049-114">-AccountName</span></span>
<span data-ttu-id="a5049-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="a5049-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5049-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5049-116">-DefaultProfile</span></span>
<span data-ttu-id="a5049-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5049-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5049-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a5049-118">-Name</span></span>
<span data-ttu-id="a5049-119">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="a5049-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5049-120">-Poolname</span><span class="sxs-lookup"><span data-stu-id="a5049-120">-PoolName</span></span>
<span data-ttu-id="a5049-121">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="a5049-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5049-122">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="a5049-122">-PoolObject</span></span>
<span data-ttu-id="a5049-123">Das Pool-Objekt, das das zurückzugebende Volume enthält</span><span class="sxs-lookup"><span data-stu-id="a5049-123">The pool object containing the volume to return</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5049-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5049-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5049-125">Die Ressourcengruppe des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="a5049-125">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5049-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5049-126">-ResourceId</span></span>
<span data-ttu-id="a5049-127">Die Ressourcen-ID des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="a5049-127">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5049-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5049-128">CommonParameters</span></span>
<span data-ttu-id="a5049-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5049-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a5049-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5049-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5049-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5049-131">INPUTS</span></span>

### <span data-ttu-id="a5049-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a5049-132">System.String</span></span>

### <span data-ttu-id="a5049-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a5049-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a5049-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5049-134">OUTPUTS</span></span>

### <span data-ttu-id="a5049-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a5049-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a5049-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5049-136">NOTES</span></span>

## <span data-ttu-id="a5049-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5049-137">RELATED LINKS</span></span>
