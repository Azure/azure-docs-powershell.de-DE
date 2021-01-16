---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300811"
---
# <span data-ttu-id="8f716-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="8f716-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="8f716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f716-102">SYNOPSIS</span></span>
<span data-ttu-id="8f716-103">Konto für Remoterendering erstellen</span><span class="sxs-lookup"><span data-stu-id="8f716-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="8f716-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f716-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f716-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f716-105">DESCRIPTION</span></span>
<span data-ttu-id="8f716-106">Erstellen Sie ein neues Remoterenderingkonto in bestimmten Abonnements, Ressourcengruppen und Regionen.</span><span class="sxs-lookup"><span data-stu-id="8f716-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="8f716-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f716-107">EXAMPLES</span></span>

### <span data-ttu-id="8f716-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8f716-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="8f716-109">Erstellen Sie im aktuellen Abonnement, in der Ressourcengruppe "rg1" und "USA, Mitte" ein neues Beispiel für das Remoterendering.</span><span class="sxs-lookup"><span data-stu-id="8f716-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="8f716-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f716-110">PARAMETERS</span></span>

### <span data-ttu-id="8f716-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f716-111">-Confirm</span></span>
<span data-ttu-id="8f716-112">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f716-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f716-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f716-113">-DefaultProfile</span></span>
<span data-ttu-id="8f716-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f716-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f716-115">-Location</span><span class="sxs-lookup"><span data-stu-id="8f716-115">-Location</span></span>
<span data-ttu-id="8f716-116">Speicherort des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="8f716-116">Remote Rendering Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f716-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8f716-117">-Name</span></span>
<span data-ttu-id="8f716-118">Kontoname des Remoterenderings.</span><span class="sxs-lookup"><span data-stu-id="8f716-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f716-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f716-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f716-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8f716-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f716-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8f716-121">-WhatIf</span></span>
<span data-ttu-id="8f716-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f716-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f716-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f716-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f716-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f716-124">CommonParameters</span></span>
<span data-ttu-id="8f716-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f716-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8f716-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f716-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f716-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f716-127">INPUTS</span></span>

### <span data-ttu-id="8f716-128">Keine</span><span class="sxs-lookup"><span data-stu-id="8f716-128">None</span></span>

## <span data-ttu-id="8f716-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f716-129">OUTPUTS</span></span>

### <span data-ttu-id="8f716-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="8f716-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="8f716-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f716-131">NOTES</span></span>

## <span data-ttu-id="8f716-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f716-132">RELATED LINKS</span></span>
