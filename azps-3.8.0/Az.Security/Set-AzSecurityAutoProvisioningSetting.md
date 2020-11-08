---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 4a54b75ce8f9361957202633c70d00431c7bdb8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003979"
---
# <span data-ttu-id="c7e4e-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="c7e4e-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="c7e4e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e4e-103">Aktualisierung der Einstellung für die automatische Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c7e4e-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="c7e4e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7e4e-104">SYNTAX</span></span>

### <span data-ttu-id="c7e4e-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7e4e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7e4e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7e4e-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7e4e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c7e4e-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7e4e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7e4e-108">DESCRIPTION</span></span>
<span data-ttu-id="c7e4e-109">Aktiviert oder deaktiviert die Einstellungen für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="c7e4e-110">Mit den Einstellungen für die automatische Bereitstellung können Sie entscheiden, ob Azure Security Center automatisch einen Sicherheitsagenten bereitstellen soll, der auf ihren VMS installiert wird.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="c7e4e-111">Der Security-Agent überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität des virtuellen Computers zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="c7e4e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7e4e-112">EXAMPLES</span></span>

### <span data-ttu-id="c7e4e-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c7e4e-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="c7e4e-114">Aktiviert die Einstellung für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="c7e4e-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c7e4e-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="c7e4e-116">Deaktiviert die Einstellung für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="c7e4e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7e4e-117">PARAMETERS</span></span>

### <span data-ttu-id="c7e4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e4e-118">-DefaultProfile</span></span>
<span data-ttu-id="c7e4e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7e4e-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="c7e4e-120">-EnableAutoProvision</span></span>
<span data-ttu-id="c7e4e-121">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="c7e4e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c7e4e-122">-InputObject</span></span>
<span data-ttu-id="c7e4e-123">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-123">Input Object.</span></span>

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

### <span data-ttu-id="c7e4e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c7e4e-124">-Name</span></span>
<span data-ttu-id="c7e4e-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="c7e4e-125">Resource name.</span></span>

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

### <span data-ttu-id="c7e4e-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c7e4e-126">-ResourceId</span></span>
<span data-ttu-id="c7e4e-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-127">Resource ID.</span></span>

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

### <span data-ttu-id="c7e4e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7e4e-128">-Confirm</span></span>
<span data-ttu-id="c7e4e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7e4e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7e4e-130">-WhatIf</span></span>
<span data-ttu-id="c7e4e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7e4e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7e4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e4e-133">CommonParameters</span></span>
<span data-ttu-id="c7e4e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7e4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e4e-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e4e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e4e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7e4e-136">INPUTS</span></span>

### <span data-ttu-id="c7e4e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c7e4e-137">System.String</span></span>

### <span data-ttu-id="c7e4e-138">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="c7e4e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="c7e4e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7e4e-139">OUTPUTS</span></span>

### <span data-ttu-id="c7e4e-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="c7e4e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="c7e4e-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7e4e-141">NOTES</span></span>

## <span data-ttu-id="c7e4e-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7e4e-142">RELATED LINKS</span></span>
