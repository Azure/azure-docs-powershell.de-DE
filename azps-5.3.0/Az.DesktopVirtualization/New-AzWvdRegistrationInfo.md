---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 3e4553fa3d11c8084f103f6e5c6b3f0c57cdb50c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387259"
---
# <span data-ttu-id="be938-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="be938-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="be938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be938-102">SYNOPSIS</span></span>
<span data-ttu-id="be938-103">Erstellen Sie Informationen zur Registrierung des virtuellen Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="be938-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="be938-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be938-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="be938-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be938-105">DESCRIPTION</span></span>
<span data-ttu-id="be938-106">Erstellen Sie Informationen zur Registrierung des virtuellen Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="be938-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="be938-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be938-107">EXAMPLES</span></span>

### <span data-ttu-id="be938-108">Beispiel 1: Erstellen eines Tokens für die Registrierung des virtuellen Windows-Desktops</span><span class="sxs-lookup"><span data-stu-id="be938-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="be938-109">Mit diesem Befehl wird ein Windows Virtual Desktop Registration Token in einem Hostpool erstellt.</span><span class="sxs-lookup"><span data-stu-id="be938-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="be938-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be938-110">PARAMETERS</span></span>

### <span data-ttu-id="be938-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be938-111">-DefaultProfile</span></span>
<span data-ttu-id="be938-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be938-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be938-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="be938-113">-ExpirationTime</span></span>
<span data-ttu-id="be938-114">Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="be938-114">Expiration Time</span></span>

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

### <span data-ttu-id="be938-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="be938-115">-HostPoolName</span></span>
<span data-ttu-id="be938-116">Name des Hostpools</span><span class="sxs-lookup"><span data-stu-id="be938-116">Host Pool Name</span></span>

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

### <span data-ttu-id="be938-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be938-117">-ResourceGroupName</span></span>
<span data-ttu-id="be938-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="be938-118">Resource Group Name</span></span>

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

### <span data-ttu-id="be938-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="be938-119">-SubscriptionId</span></span>
<span data-ttu-id="be938-120">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="be938-120">Subscription Id</span></span>

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

### <span data-ttu-id="be938-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be938-121">-Confirm</span></span>
<span data-ttu-id="be938-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be938-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be938-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="be938-123">-WhatIf</span></span>
<span data-ttu-id="be938-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be938-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be938-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be938-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be938-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be938-126">CommonParameters</span></span>
<span data-ttu-id="be938-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be938-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be938-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be938-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be938-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be938-129">INPUTS</span></span>

## <span data-ttu-id="be938-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be938-130">OUTPUTS</span></span>

### <span data-ttu-id="be938-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="be938-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="be938-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="be938-132">NOTES</span></span>

<span data-ttu-id="be938-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="be938-133">ALIASES</span></span>

## <span data-ttu-id="be938-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="be938-134">RELATED LINKS</span></span>

