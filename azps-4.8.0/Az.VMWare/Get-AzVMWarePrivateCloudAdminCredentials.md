---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009522"
---
# <span data-ttu-id="201ec-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="201ec-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="201ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="201ec-102">SYNOPSIS</span></span>
<span data-ttu-id="201ec-103">Auflisten der Administratoranmeldeinformationen für die Private Cloud</span><span class="sxs-lookup"><span data-stu-id="201ec-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="201ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="201ec-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="201ec-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="201ec-105">DESCRIPTION</span></span>
<span data-ttu-id="201ec-106">Auflisten der Administratoranmeldeinformationen für die Private Cloud</span><span class="sxs-lookup"><span data-stu-id="201ec-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="201ec-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="201ec-107">EXAMPLES</span></span>

### <span data-ttu-id="201ec-108">Beispiel 1: Abrufen von Administratoranmeldeinformationen für die Private Cloud</span><span class="sxs-lookup"><span data-stu-id="201ec-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="201ec-109">Abrufen von Administratoranmeldeinformationen für die Private Cloud</span><span class="sxs-lookup"><span data-stu-id="201ec-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="201ec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="201ec-110">PARAMETERS</span></span>

### <span data-ttu-id="201ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201ec-111">-DefaultProfile</span></span>
<span data-ttu-id="201ec-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="201ec-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="201ec-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="201ec-113">-PrivateCloudName</span></span>
<span data-ttu-id="201ec-114">Name der privaten Cloud</span><span class="sxs-lookup"><span data-stu-id="201ec-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="201ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="201ec-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="201ec-116">The name of the resource group.</span></span>
<span data-ttu-id="201ec-117">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="201ec-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="201ec-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="201ec-118">-SubscriptionId</span></span>
<span data-ttu-id="201ec-119">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="201ec-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="201ec-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="201ec-120">-Confirm</span></span>
<span data-ttu-id="201ec-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="201ec-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="201ec-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="201ec-122">-WhatIf</span></span>
<span data-ttu-id="201ec-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="201ec-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="201ec-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="201ec-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="201ec-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201ec-125">CommonParameters</span></span>
<span data-ttu-id="201ec-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201ec-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201ec-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="201ec-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201ec-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="201ec-128">INPUTS</span></span>

## <span data-ttu-id="201ec-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="201ec-129">OUTPUTS</span></span>

### <span data-ttu-id="201ec-130">Microsoft. Azure. PowerShell. Cmdlets. VMware. Models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="201ec-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="201ec-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="201ec-131">NOTES</span></span>

<span data-ttu-id="201ec-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="201ec-132">ALIASES</span></span>

## <span data-ttu-id="201ec-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="201ec-133">RELATED LINKS</span></span>

