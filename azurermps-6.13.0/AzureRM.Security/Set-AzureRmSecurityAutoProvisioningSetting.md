---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662786"
---
# <span data-ttu-id="a9d1c-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="a9d1c-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="a9d1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d1c-103">Aktualisierung der Einstellung für die automatische Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a9d1c-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9d1c-104">SYNTAX</span></span>

### <span data-ttu-id="a9d1c-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9d1c-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9d1c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9d1c-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9d1c-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a9d1c-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9d1c-108">DESCRIPTION</span></span>
<span data-ttu-id="a9d1c-109">Aktiviert oder deaktiviert die Einstellungen für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="a9d1c-110">Mit den Einstellungen für die automatische Bereitstellung können Sie entscheiden, ob Azure Security Center automatisch einen Sicherheitsagenten bereitstellen soll, der auf ihren VMS installiert wird.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="a9d1c-111">Der Security-Agent überwacht Ihre VM, um Sicherheitswarnungen zu erstellen und die Sicherheitskonformität des virtuellen Computers zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="a9d1c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9d1c-112">EXAMPLES</span></span>

### <span data-ttu-id="a9d1c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9d1c-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="a9d1c-114">Aktiviert die Einstellung für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="a9d1c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9d1c-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="a9d1c-116">Deaktiviert die Einstellung für die automatische Bereitstellung für ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="a9d1c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9d1c-117">PARAMETERS</span></span>

### <span data-ttu-id="a9d1c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d1c-118">-DefaultProfile</span></span>
<span data-ttu-id="a9d1c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d1c-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="a9d1c-120">-EnableAutoProvision</span></span>
<span data-ttu-id="a9d1c-121">Automatische Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d1c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9d1c-122">-InputObject</span></span>
<span data-ttu-id="a9d1c-123">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d1c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a9d1c-124">-Name</span></span>
<span data-ttu-id="a9d1c-125">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a9d1c-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d1c-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a9d1c-126">-ResourceId</span></span>
<span data-ttu-id="a9d1c-127">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d1c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9d1c-128">-Confirm</span></span>
<span data-ttu-id="a9d1c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d1c-130">-WhatIf</span></span>
<span data-ttu-id="a9d1c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9d1c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9d1c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d1c-133">CommonParameters</span></span>
<span data-ttu-id="a9d1c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d1c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d1c-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d1c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d1c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9d1c-136">INPUTS</span></span>

### <span data-ttu-id="a9d1c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d1c-137">System.String</span></span>
<span data-ttu-id="a9d1c-138">System. Management. Automation. Switchparameter Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="a9d1c-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="a9d1c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9d1c-139">OUTPUTS</span></span>

### <span data-ttu-id="a9d1c-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="a9d1c-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="a9d1c-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9d1c-141">NOTES</span></span>

## <span data-ttu-id="a9d1c-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9d1c-142">RELATED LINKS</span></span>
