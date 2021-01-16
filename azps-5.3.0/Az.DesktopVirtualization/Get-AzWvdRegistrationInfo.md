---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 52b2d636e9ab4dbde9cbafc69da3122828a91477
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467912"
---
# <span data-ttu-id="8987e-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="8987e-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="8987e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8987e-102">SYNOPSIS</span></span>
<span data-ttu-id="8987e-103">Hier finden Sie Informationen zur Registrierung des virtuellen Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="8987e-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="8987e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8987e-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8987e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8987e-105">DESCRIPTION</span></span>
<span data-ttu-id="8987e-106">Hier finden Sie Informationen zur Registrierung des virtuellen Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="8987e-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="8987e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8987e-107">EXAMPLES</span></span>

### <span data-ttu-id="8987e-108">Beispiel 1: Erhalten eines Tokens für die Registrierung des virtuellen Windows-Desktops</span><span class="sxs-lookup"><span data-stu-id="8987e-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="8987e-109">Dieser Befehl ruft ein Windows Virtual Desktop Registration Token in einem Hostpool ab.</span><span class="sxs-lookup"><span data-stu-id="8987e-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="8987e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8987e-110">PARAMETERS</span></span>

### <span data-ttu-id="8987e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8987e-111">-DefaultProfile</span></span>
<span data-ttu-id="8987e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8987e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8987e-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8987e-113">-HostPoolName</span></span>
<span data-ttu-id="8987e-114">Name des Hostpools</span><span class="sxs-lookup"><span data-stu-id="8987e-114">Host Pool Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8987e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8987e-115">-ResourceGroupName</span></span>
<span data-ttu-id="8987e-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="8987e-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8987e-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8987e-117">-SubscriptionId</span></span>
<span data-ttu-id="8987e-118">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="8987e-118">Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8987e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8987e-119">CommonParameters</span></span>
<span data-ttu-id="8987e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8987e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8987e-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8987e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8987e-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8987e-122">INPUTS</span></span>

## <span data-ttu-id="8987e-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8987e-123">OUTPUTS</span></span>

### <span data-ttu-id="8987e-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="8987e-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.RegistrationInfo</span></span>

## <span data-ttu-id="8987e-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8987e-125">NOTES</span></span>

<span data-ttu-id="8987e-126">ALIASE</span><span class="sxs-lookup"><span data-stu-id="8987e-126">ALIASES</span></span>

## <span data-ttu-id="8987e-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8987e-127">RELATED LINKS</span></span>

