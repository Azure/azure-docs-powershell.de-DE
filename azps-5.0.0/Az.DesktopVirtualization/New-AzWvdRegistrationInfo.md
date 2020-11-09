---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdRegistrationInfo.md
ms.openlocfilehash: 86ffd1038d834d20837b1f6a6087176e562c8844
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297027"
---
# <span data-ttu-id="79a7d-101">New-AzWvdRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="79a7d-101">New-AzWvdRegistrationInfo</span></span>

## <span data-ttu-id="79a7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="79a7d-103">Erstellen Sie Registrierungsinformationen für Windows-virtuelle Desktops.</span><span class="sxs-lookup"><span data-stu-id="79a7d-103">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="79a7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79a7d-104">SYNTAX</span></span>

```
New-AzWvdRegistrationInfo -ExpirationTime <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79a7d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79a7d-105">DESCRIPTION</span></span>
<span data-ttu-id="79a7d-106">Erstellen Sie Registrierungsinformationen für Windows-virtuelle Desktops.</span><span class="sxs-lookup"><span data-stu-id="79a7d-106">Create Windows virtual desktop registration info.</span></span>

## <span data-ttu-id="79a7d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79a7d-107">EXAMPLES</span></span>

### <span data-ttu-id="79a7d-108">Beispiel 1: Erstellen eines Windows Virtual Desktop-Registrierungs Tokens</span><span class="sxs-lookup"><span data-stu-id="79a7d-108">Example 1: Create a Windows Virtual Desktop Registration Token</span></span>
```powershell
PS C:\> New-AzWvdRegistrationInfo -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ'))

ExpirationTime       RegistrationTokenOperation Token
--------------       -------------------------- -----
4/1/2020 10:19:33 PM Update                       eyJhbGciOiJSUzI1NiIsImtpZCI6IkMyRjU1RUYxNzg0MEFCNzkzMDk2RUYzRjdEMkNBRDk0NThGNDhEOTQiLCJ0eXAiOiJKV1QifQ.eyJSZWdpc3RyYXRpb25JZCI6IjU5NGJjZWUwLTk5MjQtNDg3ZC1iOW...
```

<span data-ttu-id="79a7d-109">Mit diesem Befehl wird ein Windows Virtual Desktop-Registrierungs Token in einem Host Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="79a7d-109">This command creates a Windows Virtual Desktop Registration Token in a Host Pool.</span></span>

## <span data-ttu-id="79a7d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="79a7d-110">PARAMETERS</span></span>

### <span data-ttu-id="79a7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a7d-111">-DefaultProfile</span></span>
<span data-ttu-id="79a7d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79a7d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a7d-113">-Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="79a7d-113">-ExpirationTime</span></span>
<span data-ttu-id="79a7d-114">Ablaufzeit</span><span class="sxs-lookup"><span data-stu-id="79a7d-114">Expiration Time</span></span>

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

### <span data-ttu-id="79a7d-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="79a7d-115">-HostPoolName</span></span>
<span data-ttu-id="79a7d-116">Name des Host Pools</span><span class="sxs-lookup"><span data-stu-id="79a7d-116">Host Pool Name</span></span>

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

### <span data-ttu-id="79a7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="79a7d-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="79a7d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="79a7d-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="79a7d-119">-SubscriptionId</span></span>
<span data-ttu-id="79a7d-120">Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="79a7d-120">Subscription Id</span></span>

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

### <span data-ttu-id="79a7d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79a7d-121">-Confirm</span></span>
<span data-ttu-id="79a7d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79a7d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a7d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a7d-123">-WhatIf</span></span>
<span data-ttu-id="79a7d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79a7d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a7d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79a7d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a7d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a7d-126">CommonParameters</span></span>
<span data-ttu-id="79a7d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a7d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a7d-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79a7d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a7d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79a7d-129">INPUTS</span></span>

## <span data-ttu-id="79a7d-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79a7d-130">OUTPUTS</span></span>

### <span data-ttu-id="79a7d-131">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="79a7d-131">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IRegistrationInfo</span></span>

## <span data-ttu-id="79a7d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="79a7d-132">NOTES</span></span>

<span data-ttu-id="79a7d-133">Aliase</span><span class="sxs-lookup"><span data-stu-id="79a7d-133">ALIASES</span></span>

## <span data-ttu-id="79a7d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79a7d-134">RELATED LINKS</span></span>

