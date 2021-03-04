---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
ms.openlocfilehash: 04f914dfd54d645f3c0ae7621cafaf20099f05c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947371"
---
# <span data-ttu-id="2d1df-101">Get-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="2d1df-101">Get-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="2d1df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d1df-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1df-103">Remoterenderingkonto erhalten</span><span class="sxs-lookup"><span data-stu-id="2d1df-103">Get Remote Rendering Account</span></span>

## <span data-ttu-id="2d1df-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d1df-104">SYNTAX</span></span>

### <span data-ttu-id="2d1df-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d1df-105">ListParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d1df-106">GetParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d1df-106">GetParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d1df-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d1df-107">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d1df-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d1df-108">DESCRIPTION</span></span>
<span data-ttu-id="2d1df-109">Sie können Remoterenderingkontos in bestimmten Abonnement- und Ressourcengruppen erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="2d1df-109">Get or list Remote Rendering Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="2d1df-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2d1df-110">EXAMPLES</span></span>

### <span data-ttu-id="2d1df-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d1df-111">Example 1</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/RemoteRenderingAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="2d1df-112">Listen Sie alle Remoterendering-Konten in der Ressourcengruppe "rg1" auf.</span><span class="sxs-lookup"><span data-stu-id="2d1df-112">List all Remote Rendering Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="2d1df-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2d1df-113">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="2d1df-114">Holen Sie sich das "Beispiel" des Remoterenderingkontos in der Ressourcengruppe "rg1".</span><span class="sxs-lookup"><span data-stu-id="2d1df-114">Get Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="2d1df-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2d1df-115">PARAMETERS</span></span>

### <span data-ttu-id="2d1df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1df-116">-DefaultProfile</span></span>
<span data-ttu-id="2d1df-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d1df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d1df-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2d1df-118">-Name</span></span>
<span data-ttu-id="2d1df-119">Name des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="2d1df-119">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d1df-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d1df-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d1df-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2d1df-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d1df-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d1df-122">-ResourceId</span></span>
<span data-ttu-id="2d1df-123">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="2d1df-123">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="2d1df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1df-124">CommonParameters</span></span>
<span data-ttu-id="2d1df-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d1df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2d1df-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d1df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1df-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2d1df-127">INPUTS</span></span>

### <span data-ttu-id="2d1df-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2d1df-128">System.String</span></span>

## <span data-ttu-id="2d1df-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2d1df-129">OUTPUTS</span></span>

### <span data-ttu-id="2d1df-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="2d1df-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="2d1df-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2d1df-131">NOTES</span></span>

## <span data-ttu-id="2d1df-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2d1df-132">RELATED LINKS</span></span>
