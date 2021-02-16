---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150812"
---
# <span data-ttu-id="76a92-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="76a92-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="76a92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76a92-102">SYNOPSIS</span></span>
<span data-ttu-id="76a92-103">Aktualisiert die Einstellung für die automatische Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="76a92-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="76a92-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76a92-104">SYNTAX</span></span>

### <span data-ttu-id="76a92-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="76a92-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76a92-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="76a92-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76a92-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="76a92-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a92-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="76a92-108">DESCRIPTION</span></span>
<span data-ttu-id="76a92-109">Aktiviert oder deaktiviert die Einstellungen für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76a92-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="76a92-110">Mit den Einstellungen für die automatische Bereitstellung können Sie entscheiden, ob Azure Security Center automatisch einen Sicherheits-Agent bereitstellen soll, der auf Ihren VMs installiert wird.</span><span class="sxs-lookup"><span data-stu-id="76a92-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="76a92-111">Der Sicherheitsmitarbeiter überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität der VM zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="76a92-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="76a92-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="76a92-112">EXAMPLES</span></span>

### <span data-ttu-id="76a92-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76a92-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="76a92-114">Aktiviert die Einstellung für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76a92-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="76a92-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="76a92-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="76a92-116">Deaktiviert die Einstellung für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76a92-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="76a92-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76a92-117">PARAMETERS</span></span>

### <span data-ttu-id="76a92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a92-118">-DefaultProfile</span></span>
<span data-ttu-id="76a92-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76a92-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a92-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="76a92-120">-EnableAutoProvision</span></span>
<span data-ttu-id="76a92-121">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="76a92-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76a92-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76a92-122">-InputObject</span></span>
<span data-ttu-id="76a92-123">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="76a92-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76a92-124">-Name</span><span class="sxs-lookup"><span data-stu-id="76a92-124">-Name</span></span>
<span data-ttu-id="76a92-125">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="76a92-125">Resource name.</span></span>

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

### <span data-ttu-id="76a92-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76a92-126">-ResourceId</span></span>
<span data-ttu-id="76a92-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="76a92-127">Resource ID.</span></span>

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

### <span data-ttu-id="76a92-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76a92-128">-Confirm</span></span>
<span data-ttu-id="76a92-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76a92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a92-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="76a92-130">-WhatIf</span></span>
<span data-ttu-id="76a92-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76a92-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76a92-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76a92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a92-133">CommonParameters</span></span>
<span data-ttu-id="76a92-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a92-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76a92-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a92-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="76a92-136">INPUTS</span></span>

### <span data-ttu-id="76a92-137">System.String</span><span class="sxs-lookup"><span data-stu-id="76a92-137">System.String</span></span>

### <span data-ttu-id="76a92-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="76a92-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="76a92-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="76a92-139">OUTPUTS</span></span>

### <span data-ttu-id="76a92-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="76a92-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="76a92-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="76a92-141">NOTES</span></span>

## <span data-ttu-id="76a92-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="76a92-142">RELATED LINKS</span></span>
