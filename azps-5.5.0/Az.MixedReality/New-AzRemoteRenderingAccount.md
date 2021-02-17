---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147433"
---
# <span data-ttu-id="4f738-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="4f738-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="4f738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f738-102">SYNOPSIS</span></span>
<span data-ttu-id="4f738-103">Konto für Remoterendering erstellen</span><span class="sxs-lookup"><span data-stu-id="4f738-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="4f738-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f738-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f738-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f738-105">DESCRIPTION</span></span>
<span data-ttu-id="4f738-106">Erstellen Sie ein neues Remoterenderingkonto in bestimmten Abonnements, Ressourcengruppen und Regionen.</span><span class="sxs-lookup"><span data-stu-id="4f738-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="4f738-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f738-107">EXAMPLES</span></span>

### <span data-ttu-id="4f738-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4f738-108">Example 1</span></span>
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

<span data-ttu-id="4f738-109">Erstellen Sie im aktuellen Abonnement, in der Ressourcengruppe "rg1" und "USA, Mitte" ein neues Beispiel für das Remoterendering.</span><span class="sxs-lookup"><span data-stu-id="4f738-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="4f738-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f738-110">PARAMETERS</span></span>

### <span data-ttu-id="4f738-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f738-111">-Confirm</span></span>
<span data-ttu-id="4f738-112">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f738-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f738-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f738-113">-DefaultProfile</span></span>
<span data-ttu-id="4f738-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f738-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f738-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4f738-115">-Location</span></span>
<span data-ttu-id="4f738-116">Speicherort des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="4f738-116">Remote Rendering Account Location.</span></span>

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

### <span data-ttu-id="4f738-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4f738-117">-Name</span></span>
<span data-ttu-id="4f738-118">Kontoname des Remoterenderings.</span><span class="sxs-lookup"><span data-stu-id="4f738-118">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="4f738-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f738-119">-ResourceGroupName</span></span>
<span data-ttu-id="4f738-120">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4f738-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="4f738-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f738-121">-WhatIf</span></span>
<span data-ttu-id="4f738-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f738-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f738-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f738-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f738-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f738-124">CommonParameters</span></span>
<span data-ttu-id="4f738-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f738-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4f738-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f738-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f738-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f738-127">INPUTS</span></span>

### <span data-ttu-id="4f738-128">Keine</span><span class="sxs-lookup"><span data-stu-id="4f738-128">None</span></span>

## <span data-ttu-id="4f738-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f738-129">OUTPUTS</span></span>

### <span data-ttu-id="4f738-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="4f738-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="4f738-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f738-131">NOTES</span></span>

## <span data-ttu-id="4f738-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f738-132">RELATED LINKS</span></span>
