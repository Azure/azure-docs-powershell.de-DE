---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178222"
---
# <span data-ttu-id="538f7-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="538f7-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="538f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="538f7-102">SYNOPSIS</span></span>
<span data-ttu-id="538f7-103">Ruft die Einstellungen für die automatische Bereitstellung der Sicherheit ab</span><span class="sxs-lookup"><span data-stu-id="538f7-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="538f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="538f7-104">SYNTAX</span></span>

### <span data-ttu-id="538f7-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="538f7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="538f7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="538f7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="538f7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="538f7-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="538f7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="538f7-108">DESCRIPTION</span></span>
<span data-ttu-id="538f7-109">Mit den Einstellungen für die automatische Bereitstellung können Sie entscheiden, ob Azure Security Center automatisch einen Sicherheitsagenten bereitstellen soll, der auf ihren VMS installiert wird.</span><span class="sxs-lookup"><span data-stu-id="538f7-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="538f7-110">Der Security-Agent überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität des virtuellen Computers zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="538f7-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="538f7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="538f7-111">EXAMPLES</span></span>

### <span data-ttu-id="538f7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="538f7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="538f7-113">Ruft die Einstellung für die automatische Bereitstellung für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="538f7-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="538f7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="538f7-114">PARAMETERS</span></span>

### <span data-ttu-id="538f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="538f7-115">-DefaultProfile</span></span>
<span data-ttu-id="538f7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="538f7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="538f7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="538f7-117">-Name</span></span>
<span data-ttu-id="538f7-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="538f7-118">Resource name.</span></span>

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

### <span data-ttu-id="538f7-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="538f7-119">-ResourceId</span></span>
<span data-ttu-id="538f7-120">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="538f7-120">Resource ID.</span></span>

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

### <span data-ttu-id="538f7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="538f7-121">CommonParameters</span></span>
<span data-ttu-id="538f7-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="538f7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="538f7-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="538f7-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="538f7-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="538f7-124">INPUTS</span></span>

### <span data-ttu-id="538f7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="538f7-125">System.String</span></span>

## <span data-ttu-id="538f7-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="538f7-126">OUTPUTS</span></span>

### <span data-ttu-id="538f7-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="538f7-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="538f7-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="538f7-128">NOTES</span></span>

## <span data-ttu-id="538f7-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="538f7-129">RELATED LINKS</span></span>
