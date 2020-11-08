---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: e9397a2a62ebaa4d26e0d36aaad3fbe03bad137e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010152"
---
# <span data-ttu-id="5a418-101">Get-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a418-101">Get-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="5a418-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a418-102">SYNOPSIS</span></span>
<span data-ttu-id="5a418-103">Abrufen von Schlüsseln des Remote Rendering-Kontos</span><span class="sxs-lookup"><span data-stu-id="5a418-103">Get keys of Remote Rendering Account</span></span>

## <span data-ttu-id="5a418-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a418-104">SYNTAX</span></span>

### <span data-ttu-id="5a418-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a418-105">DefaultParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a418-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a418-106">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a418-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a418-107">PipelineParameterSet</span></span>
```
Get-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a418-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a418-108">DESCRIPTION</span></span>
<span data-ttu-id="5a418-109">Abrufen von Entwickler Schlüsseln des Remote Rendering-Kontos</span><span class="sxs-lookup"><span data-stu-id="5a418-109">Get developer keys of Remote Rendering Account.</span></span>

## <span data-ttu-id="5a418-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a418-110">EXAMPLES</span></span>

### <span data-ttu-id="5a418-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5a418-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="5a418-112">Holen Sie sich die Entwickler Schlüssel des Remote Rendering-Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="5a418-112">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="5a418-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5a418-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | Get-AzRemoteRenderingAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="5a418-114">Holen Sie sich die Entwickler Schlüssel des Remote Rendering-Kontos "Beispiel" aus dem aktuellen Abonnement und der Ressourcengruppe "RG1" mit Piping.</span><span class="sxs-lookup"><span data-stu-id="5a418-114">Get developer keys of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="5a418-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a418-115">PARAMETERS</span></span>

### <span data-ttu-id="5a418-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a418-116">-DefaultProfile</span></span>
<span data-ttu-id="5a418-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5a418-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a418-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a418-118">-InputObject</span></span>
<span data-ttu-id="5a418-119">Das benutzerdefinierte Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="5a418-119">The custom domain object.</span></span>

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

### <span data-ttu-id="5a418-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5a418-120">-Name</span></span>
<span data-ttu-id="5a418-121">Name des Remote Rendering-Kontos</span><span class="sxs-lookup"><span data-stu-id="5a418-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="5a418-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a418-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a418-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5a418-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5a418-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5a418-124">-ResourceId</span></span>
<span data-ttu-id="5a418-125">Ressourcen-ID des Remote Rendering-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5a418-125">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="5a418-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a418-126">CommonParameters</span></span>
<span data-ttu-id="5a418-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a418-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5a418-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a418-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a418-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a418-129">INPUTS</span></span>

### <span data-ttu-id="5a418-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5a418-130">System.String</span></span>

### <span data-ttu-id="5a418-131">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="5a418-131">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="5a418-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a418-132">OUTPUTS</span></span>

### <span data-ttu-id="5a418-133">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5a418-133">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="5a418-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a418-134">NOTES</span></span>

## <span data-ttu-id="5a418-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a418-135">RELATED LINKS</span></span>
