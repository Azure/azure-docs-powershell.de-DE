---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: b48222344e9a9fdb958073a658717d1cafa057f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946872"
---
# <span data-ttu-id="bdb8c-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="bdb8c-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="bdb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb8c-103">Ruft die Einstellungen für die automatische Sicherheitsbereitstellung ab.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="bdb8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdb8c-104">SYNTAX</span></span>

### <span data-ttu-id="bdb8c-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="bdb8c-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb8c-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="bdb8c-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bdb8c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb8c-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdb8c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdb8c-108">DESCRIPTION</span></span>
<span data-ttu-id="bdb8c-109">Mit den Einstellungen für automatische Bereitstellung können Sie entscheiden, ob Azure Security Center automatisch einen Sicherheits-Agent bereitstellen soll, der auf Ihren VMs installiert wird.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="bdb8c-110">Der Sicherheits-Agent überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität der VM zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="bdb8c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bdb8c-111">EXAMPLES</span></span>

### <span data-ttu-id="bdb8c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bdb8c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="bdb8c-113">Ruft die Einstellung für die automatische Bereitstellung für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="bdb8c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bdb8c-114">PARAMETERS</span></span>

### <span data-ttu-id="bdb8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb8c-115">-DefaultProfile</span></span>
<span data-ttu-id="bdb8c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb8c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bdb8c-117">-Name</span></span>
<span data-ttu-id="bdb8c-118">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-118">Resource name.</span></span>

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

### <span data-ttu-id="bdb8c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb8c-119">-ResourceId</span></span>
<span data-ttu-id="bdb8c-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-120">Resource ID.</span></span>

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

### <span data-ttu-id="bdb8c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb8c-121">CommonParameters</span></span>
<span data-ttu-id="bdb8c-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb8c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb8c-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdb8c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb8c-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bdb8c-124">INPUTS</span></span>

### <span data-ttu-id="bdb8c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bdb8c-125">System.String</span></span>

## <span data-ttu-id="bdb8c-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bdb8c-126">OUTPUTS</span></span>

### <span data-ttu-id="bdb8c-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="bdb8c-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="bdb8c-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="bdb8c-128">NOTES</span></span>

## <span data-ttu-id="bdb8c-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="bdb8c-129">RELATED LINKS</span></span>
