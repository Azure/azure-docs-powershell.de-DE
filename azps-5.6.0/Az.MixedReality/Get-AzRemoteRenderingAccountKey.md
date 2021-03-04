---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: 03cb387b77dc2f003277b9f04a482f88a8da86fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921952"
---
# <span data-ttu-id="5b6e8-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="5b6e8-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="5b6e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b6e8-102">SYNOPSIS</span></span>
<span data-ttu-id="5b6e8-103">Schlüssel des Remoterenderungskontos</span><span class="sxs-lookup"><span data-stu-id="5b6e8-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="5b6e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b6e8-104">SYNTAX</span></span>

### <span data-ttu-id="5b6e8-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5b6e8-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b6e8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b6e8-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b6e8-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b6e8-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b6e8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5b6e8-108">DESCRIPTION</span></span>
<span data-ttu-id="5b6e8-109">Holen Sie sich Entwicklerschlüssel des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="5b6e8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5b6e8-110">EXAMPLES</span></span>

### <span data-ttu-id="5b6e8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b6e8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="5b6e8-112">Holen Sie sich Entwicklerschlüssel des Remoterenderingkontos "Example" aus dem aktuellen Abonnement und der Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="5b6e8-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="5b6e8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b6e8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="5b6e8-114">Holen Sie sich Entwicklerschlüssel des Remoterenderingkontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "rg1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="5b6e8-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5b6e8-115">PARAMETERS</span></span>

### <span data-ttu-id="5b6e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b6e8-116">-DefaultProfile</span></span>
<span data-ttu-id="5b6e8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b6e8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b6e8-118">-InputObject</span></span>
<span data-ttu-id="5b6e8-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6e8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b6e8-120">-Name</span></span>
<span data-ttu-id="5b6e8-121">Name des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6e8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b6e8-122">-ResourceGroupName</span></span>
<span data-ttu-id="5b6e8-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b6e8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b6e8-124">-ResourceId</span></span>
<span data-ttu-id="5b6e8-125">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-125">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b6e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b6e8-126">CommonParameters</span></span>
<span data-ttu-id="5b6e8-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b6e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b6e8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b6e8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b6e8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5b6e8-129">INPUTS</span></span>

### <span data-ttu-id="5b6e8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5b6e8-130">System.String</span></span>

### <span data-ttu-id="5b6e8-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="5b6e8-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="5b6e8-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5b6e8-132">OUTPUTS</span></span>

### <span data-ttu-id="5b6e8-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5b6e8-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="5b6e8-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5b6e8-134">NOTES</span></span>

## <span data-ttu-id="5b6e8-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5b6e8-135">RELATED LINKS</span></span>
