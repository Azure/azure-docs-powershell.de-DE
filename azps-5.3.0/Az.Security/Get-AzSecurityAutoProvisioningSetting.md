---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472040"
---
# <span data-ttu-id="fbac3-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="fbac3-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="fbac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbac3-102">SYNOPSIS</span></span>
<span data-ttu-id="fbac3-103">Ruft die Sicherheitseinstellungen für die automatische Bereitstellung ab.</span><span class="sxs-lookup"><span data-stu-id="fbac3-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="fbac3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbac3-104">SYNTAX</span></span>

### <span data-ttu-id="fbac3-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbac3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbac3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="fbac3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbac3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbac3-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbac3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbac3-108">DESCRIPTION</span></span>
<span data-ttu-id="fbac3-109">Mit den Einstellungen für die automatische Bereitstellung können Sie entscheiden, ob Azure Security Center automatisch einen Sicherheits-Agent bereitstellen soll, der auf Ihren VMs installiert wird.</span><span class="sxs-lookup"><span data-stu-id="fbac3-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="fbac3-110">Der Sicherheitsmitarbeiter überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität der VM zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="fbac3-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="fbac3-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbac3-111">EXAMPLES</span></span>

### <span data-ttu-id="fbac3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbac3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="fbac3-113">Ruft die Einstellung für die automatische Bereitstellung für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fbac3-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="fbac3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbac3-114">PARAMETERS</span></span>

### <span data-ttu-id="fbac3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbac3-115">-DefaultProfile</span></span>
<span data-ttu-id="fbac3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbac3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbac3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fbac3-117">-Name</span></span>
<span data-ttu-id="fbac3-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="fbac3-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbac3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbac3-119">-ResourceId</span></span>
<span data-ttu-id="fbac3-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fbac3-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbac3-121">CommonParameters</span></span>
<span data-ttu-id="fbac3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbac3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbac3-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbac3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbac3-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbac3-124">INPUTS</span></span>

### <span data-ttu-id="fbac3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fbac3-125">System.String</span></span>

## <span data-ttu-id="fbac3-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbac3-126">OUTPUTS</span></span>

### <span data-ttu-id="fbac3-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="fbac3-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="fbac3-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbac3-128">NOTES</span></span>

## <span data-ttu-id="fbac3-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbac3-129">RELATED LINKS</span></span>
