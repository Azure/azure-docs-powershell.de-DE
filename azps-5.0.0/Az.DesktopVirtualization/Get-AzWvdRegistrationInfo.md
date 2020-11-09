---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdRegistrationInfo.md
ms.openlocfilehash: 0f82c80e9f06abd5a2189bbee665de58ee6a3528
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297069"
---
# <span data-ttu-id="8b723-101">Get-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="8b723-101">Get-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="8b723-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b723-102">SYNOPSIS</span></span>
<span data-ttu-id="8b723-103">Abrufen der Registrierungsinformationen für Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="8b723-103">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="8b723-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b723-104">SYNTAX</span></span>

```
Get-AzWvdRegistrationInfo -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8b723-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b723-105">DESCRIPTION</span></span>
<span data-ttu-id="8b723-106">Abrufen der Registrierungsinformationen für Windows Virtual Desktop.</span><span class="sxs-lookup"><span data-stu-id="8b723-106">Get the Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="8b723-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b723-107">EXAMPLES</span></span>

### <span data-ttu-id="8b723-108">Beispiel 1: Abrufen eines Windows-virtuellen Desktop Registrierungs Tokens</span><span class="sxs-lookup"><span data-stu-id="8b723-108">Example 1: Get a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> Get-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM None                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="8b723-109">Dieser Befehl ruft ein Windows Virtual Desktop-Registrierungs Token in einem Host Pool ab.</span><span class="sxs-lookup"><span data-stu-id="8b723-109">This command gets a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="8b723-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b723-110">PARAMETERS</span></span>

### <span data-ttu-id="8b723-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b723-111">-DefaultProfile</span></span>
<span data-ttu-id="8b723-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b723-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b723-113">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8b723-113">-HostPoolName</span></span>
<span data-ttu-id="8b723-114">Name des Host Pools</span><span class="sxs-lookup"><span data-stu-id="8b723-114">Host Pool Name</span></span>

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

### <span data-ttu-id="8b723-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b723-115">-ResourceGroupName</span></span>
<span data-ttu-id="8b723-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8b723-116">Resource Group Name</span></span>

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

### <span data-ttu-id="8b723-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8b723-117">-SubscriptionId</span></span>
<span data-ttu-id="8b723-118">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="8b723-118">Subscription Id</span></span>

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

### <span data-ttu-id="8b723-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b723-119">CommonParameters</span></span>
<span data-ttu-id="8b723-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b723-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b723-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b723-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b723-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b723-122">INPUTS</span></span>

## <span data-ttu-id="8b723-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b723-123">OUTPUTS</span></span>

### <span data-ttu-id="8b723-124">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. RegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="8b723-124">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.RegistrationInfo</span></span>

## <span data-ttu-id="8b723-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b723-125">NOTES</span></span>

<span data-ttu-id="8b723-126">Aliase</span><span class="sxs-lookup"><span data-stu-id="8b723-126">ALIASES</span></span>

## <span data-ttu-id="8b723-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b723-127">RELATED LINKS</span></span>

