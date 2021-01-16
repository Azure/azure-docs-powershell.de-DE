---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 2268135ebd1e1c504aae7462730d104e842f288f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294058"
---
# <span data-ttu-id="d2053-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="d2053-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="d2053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2053-102">SYNOPSIS</span></span>
<span data-ttu-id="d2053-103">Erstellen Sie Informationen zur Registrierung des virtuellen Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="d2053-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d2053-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2053-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2053-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2053-105">DESCRIPTION</span></span>
<span data-ttu-id="d2053-106">Erstellen Sie Informationen zur Registrierung des virtuellen Windows-Desktops.</span><span class="sxs-lookup"><span data-stu-id="d2053-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="d2053-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2053-107">EXAMPLES</span></span>

### <span data-ttu-id="d2053-108">Beispiel 1: Erstellen eines Tokens für die Registrierung des virtuellen Windows-Desktops</span><span class="sxs-lookup"><span data-stu-id="d2053-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="d2053-109">Mit diesem Befehl wird ein Windows Virtual Desktop Registration Token in einem Hostpool erstellt.</span><span class="sxs-lookup"><span data-stu-id="d2053-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="d2053-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2053-110">PARAMETERS</span></span>

### <span data-ttu-id="d2053-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2053-111">-DefaultProfile</span></span>
<span data-ttu-id="d2053-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2053-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2053-113">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="d2053-113">-ExpirationTime</span></span>
<span data-ttu-id="d2053-114">Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="d2053-114">Expiration Time</span></span>

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

### <span data-ttu-id="d2053-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d2053-115">-HostPoolName</span></span>
<span data-ttu-id="d2053-116">Name des Hostpools</span><span class="sxs-lookup"><span data-stu-id="d2053-116">Host Pool Name</span></span>

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

### <span data-ttu-id="d2053-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2053-117">-ResourceGroupName</span></span>
<span data-ttu-id="d2053-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d2053-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d2053-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2053-119">-SubscriptionId</span></span>
<span data-ttu-id="d2053-120">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="d2053-120">Subscription Id</span></span>

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

### <span data-ttu-id="d2053-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2053-121">-Confirm</span></span>
<span data-ttu-id="d2053-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2053-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2053-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d2053-123">-WhatIf</span></span>
<span data-ttu-id="d2053-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2053-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2053-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2053-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2053-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2053-126">CommonParameters</span></span>
<span data-ttu-id="d2053-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2053-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2053-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2053-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2053-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2053-129">INPUTS</span></span>

## <span data-ttu-id="d2053-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2053-130">OUTPUTS</span></span>

### <span data-ttu-id="d2053-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="d2053-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="d2053-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2053-132">NOTES</span></span>

<span data-ttu-id="d2053-133">ALIASE</span><span class="sxs-lookup"><span data-stu-id="d2053-133">ALIASES</span></span>

## <span data-ttu-id="d2053-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2053-134">RELATED LINKS</span></span>

