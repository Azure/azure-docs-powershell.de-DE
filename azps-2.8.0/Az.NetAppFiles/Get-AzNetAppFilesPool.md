---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 56613276907772cfe3f2cbd99810ff247485913f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822607"
---
# <span data-ttu-id="33eb9-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="33eb9-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="33eb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="33eb9-103">Ruft Details eines Azure NetApp-Dateien (ANF)-Pools ab.</span><span class="sxs-lookup"><span data-stu-id="33eb9-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="33eb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33eb9-104">SYNTAX</span></span>

### <span data-ttu-id="33eb9-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="33eb9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33eb9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33eb9-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33eb9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33eb9-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33eb9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33eb9-108">DESCRIPTION</span></span>
<span data-ttu-id="33eb9-109">Das Cmdlet " **Get-AzNetAppFilesPool** " ruft Details zu einem ANF-Pool ab.</span><span class="sxs-lookup"><span data-stu-id="33eb9-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="33eb9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33eb9-110">EXAMPLES</span></span>

### <span data-ttu-id="33eb9-111">Beispiel 1: Abrufen eines ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="33eb9-111">Example 1: Get an ANF pool</span></span>
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
ProvisioningState : Succeeded
```

<span data-ttu-id="33eb9-112">Dieser Befehl ruft das Konto mit dem Namen MyAnfPool aus dem Konto "MyAnfAccount" ab.</span><span class="sxs-lookup"><span data-stu-id="33eb9-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="33eb9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="33eb9-113">PARAMETERS</span></span>

### <span data-ttu-id="33eb9-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="33eb9-114">-AccountName</span></span>
<span data-ttu-id="33eb9-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="33eb9-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="33eb9-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="33eb9-116">-AccountObject</span></span>
<span data-ttu-id="33eb9-117">Das Kontoobjekt, das den zurückzugebenden Pool enthält</span><span class="sxs-lookup"><span data-stu-id="33eb9-117">The account object containing the pool to return</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33eb9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33eb9-118">-DefaultProfile</span></span>
<span data-ttu-id="33eb9-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33eb9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33eb9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="33eb9-120">-Name</span></span>
<span data-ttu-id="33eb9-121">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="33eb9-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33eb9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33eb9-122">-ResourceGroupName</span></span>
<span data-ttu-id="33eb9-123">Die Ressourcengruppe des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="33eb9-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="33eb9-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="33eb9-124">-ResourceId</span></span>
<span data-ttu-id="33eb9-125">Die Ressourcen-ID des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="33eb9-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="33eb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33eb9-126">CommonParameters</span></span>
<span data-ttu-id="33eb9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33eb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="33eb9-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33eb9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33eb9-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33eb9-129">INPUTS</span></span>

### <span data-ttu-id="33eb9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="33eb9-130">System.String</span></span>

### <span data-ttu-id="33eb9-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="33eb9-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="33eb9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33eb9-132">OUTPUTS</span></span>

### <span data-ttu-id="33eb9-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="33eb9-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="33eb9-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="33eb9-134">NOTES</span></span>

## <span data-ttu-id="33eb9-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33eb9-135">RELATED LINKS</span></span>
