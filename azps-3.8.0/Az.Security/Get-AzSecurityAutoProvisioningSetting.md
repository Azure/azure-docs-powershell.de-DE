---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 6c926b606cc764abcf3627c725596deffda395b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004395"
---
# <span data-ttu-id="2dbd9-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="2dbd9-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="2dbd9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2dbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbd9-103">Ruft die Einstellungen für die automatische Bereitstellung der Sicherheit ab</span><span class="sxs-lookup"><span data-stu-id="2dbd9-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="2dbd9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dbd9-104">SYNTAX</span></span>

### <span data-ttu-id="2dbd9-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="2dbd9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dbd9-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2dbd9-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dbd9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dbd9-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dbd9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2dbd9-108">DESCRIPTION</span></span>
<span data-ttu-id="2dbd9-109">Mit den Einstellungen für die automatische Bereitstellung können Sie entscheiden, ob Azure Security Center automatisch einen Sicherheitsagenten bereitstellen soll, der auf ihren VMS installiert wird.</span><span class="sxs-lookup"><span data-stu-id="2dbd9-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="2dbd9-110">Der Security-Agent überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität des virtuellen Computers zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="2dbd9-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="2dbd9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dbd9-111">EXAMPLES</span></span>

### <span data-ttu-id="2dbd9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2dbd9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="2dbd9-113">Ruft die Einstellung für die automatische Bereitstellung für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="2dbd9-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="2dbd9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dbd9-114">PARAMETERS</span></span>

### <span data-ttu-id="2dbd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbd9-115">-DefaultProfile</span></span>
<span data-ttu-id="2dbd9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2dbd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dbd9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2dbd9-117">-Name</span></span>
<span data-ttu-id="2dbd9-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="2dbd9-118">Resource name.</span></span>

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

### <span data-ttu-id="2dbd9-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2dbd9-119">-ResourceId</span></span>
<span data-ttu-id="2dbd9-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2dbd9-120">Resource ID.</span></span>

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

### <span data-ttu-id="2dbd9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbd9-121">CommonParameters</span></span>
<span data-ttu-id="2dbd9-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbd9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbd9-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dbd9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbd9-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2dbd9-124">INPUTS</span></span>

### <span data-ttu-id="2dbd9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2dbd9-125">System.String</span></span>

## <span data-ttu-id="2dbd9-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2dbd9-126">OUTPUTS</span></span>

### <span data-ttu-id="2dbd9-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="2dbd9-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="2dbd9-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="2dbd9-128">NOTES</span></span>

## <span data-ttu-id="2dbd9-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2dbd9-129">RELATED LINKS</span></span>
