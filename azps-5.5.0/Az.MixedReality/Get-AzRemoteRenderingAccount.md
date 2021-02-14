---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzRemoteRenderingAccount.md
ms.openlocfilehash: 9d4faa4a51352902330286722a005fae1b42bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161332"
---
# <span data-ttu-id="b97d8-101">Get-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="b97d8-101">Get-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="b97d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b97d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b97d8-103">Konto für Remoterendering erhalten</span><span class="sxs-lookup"><span data-stu-id="b97d8-103">Get Remote Rendering Account</span></span>

## <span data-ttu-id="b97d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b97d8-104">SYNTAX</span></span>

### <span data-ttu-id="b97d8-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b97d8-105">ListParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97d8-106">GetParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b97d8-106">GetParameterSet (Default)</span></span>
```
Get-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b97d8-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b97d8-107">ResourceIdParameterSet</span></span>
```
Get-AzRemoteRenderingAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b97d8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b97d8-108">DESCRIPTION</span></span>
<span data-ttu-id="b97d8-109">Sie können Remoterenderingkonto(en) in bestimmten Abonnement- und Ressourcengruppen erhalten oder auflisten.</span><span class="sxs-lookup"><span data-stu-id="b97d8-109">Get or list Remote Rendering Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="b97d8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b97d8-110">EXAMPLES</span></span>

### <span data-ttu-id="b97d8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b97d8-111">Example 1</span></span>
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

<span data-ttu-id="b97d8-112">Listen Sie alle Konten für das Remoterendering in der Ressourcengruppe "rg1" auf.</span><span class="sxs-lookup"><span data-stu-id="b97d8-112">List all Remote Rendering Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="b97d8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b97d8-113">Example 2</span></span>
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

<span data-ttu-id="b97d8-114">"Beispiel" des Remoterenderingkontos in der Ressourcengruppe "rg1" erhalten.</span><span class="sxs-lookup"><span data-stu-id="b97d8-114">Get Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="b97d8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b97d8-115">PARAMETERS</span></span>

### <span data-ttu-id="b97d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97d8-116">-DefaultProfile</span></span>
<span data-ttu-id="b97d8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b97d8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b97d8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b97d8-118">-Name</span></span>
<span data-ttu-id="b97d8-119">Kontoname des Remoterenderings.</span><span class="sxs-lookup"><span data-stu-id="b97d8-119">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="b97d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b97d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="b97d8-121">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b97d8-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="b97d8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b97d8-122">-ResourceId</span></span>
<span data-ttu-id="b97d8-123">Ressourcen-ID des Remoterenderingkontos.</span><span class="sxs-lookup"><span data-stu-id="b97d8-123">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="b97d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97d8-124">CommonParameters</span></span>
<span data-ttu-id="b97d8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b97d8-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b97d8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97d8-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b97d8-127">INPUTS</span></span>

### <span data-ttu-id="b97d8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b97d8-128">System.String</span></span>

## <span data-ttu-id="b97d8-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b97d8-129">OUTPUTS</span></span>

### <span data-ttu-id="b97d8-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="b97d8-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="b97d8-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b97d8-131">NOTES</span></span>

## <span data-ttu-id="b97d8-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b97d8-132">RELATED LINKS</span></span>
