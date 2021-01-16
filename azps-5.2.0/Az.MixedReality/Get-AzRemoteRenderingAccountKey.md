---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291923"
---
# <span data-ttu-id="8f955-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="8f955-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="8f955-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f955-102">SYNOPSIS</span></span>
<span data-ttu-id="8f955-103">Schlüssel des Remoterenderingkontos</span><span class="sxs-lookup"><span data-stu-id="8f955-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="8f955-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f955-104">SYNTAX</span></span>

### <span data-ttu-id="8f955-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8f955-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f955-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f955-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f955-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f955-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f955-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f955-108">DESCRIPTION</span></span>
<span data-ttu-id="8f955-109">Holen Sie sich die Entwicklerschlüssel für das Remoterenderingkonto.</span><span class="sxs-lookup"><span data-stu-id="8f955-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="8f955-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f955-110">EXAMPLES</span></span>

### <span data-ttu-id="8f955-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f955-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="8f955-112">Holen Sie sich die Entwicklerschlüssel des Remoterenderingkontos "example" aus der aktuellen Abonnement- und Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="8f955-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="8f955-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8f955-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="8f955-114">Holen Sie sich die Entwicklerschlüssel des Beispiels für das Remoterenderingkonto aus der aktuellen Abonnement- und Ressourcengruppe "rg1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="8f955-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="8f955-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f955-115">PARAMETERS</span></span>

### <span data-ttu-id="8f955-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f955-116">-DefaultProfile</span></span>
<span data-ttu-id="8f955-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f955-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f955-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f955-118">-InputObject</span></span>
<span data-ttu-id="8f955-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="8f955-119">The custom domain object.</span></span>

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

### <span data-ttu-id="8f955-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8f955-120">-Name</span></span>
<span data-ttu-id="8f955-121">Kontoname des Remoterenderings.</span><span class="sxs-lookup"><span data-stu-id="8f955-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="8f955-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f955-122">-ResourceGroupName</span></span>
<span data-ttu-id="8f955-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8f955-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="8f955-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f955-124">-ResourceId</span></span>
<span data-ttu-id="8f955-125">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="8f955-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="8f955-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f955-126">CommonParameters</span></span>
<span data-ttu-id="8f955-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f955-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8f955-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f955-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f955-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f955-129">INPUTS</span></span>

### <span data-ttu-id="8f955-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8f955-130">System.String</span></span>

### <span data-ttu-id="8f955-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="8f955-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="8f955-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f955-132">OUTPUTS</span></span>

### <span data-ttu-id="8f955-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8f955-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="8f955-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f955-134">NOTES</span></span>

## <span data-ttu-id="8f955-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f955-135">RELATED LINKS</span></span>
