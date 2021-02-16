---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: 761d34b4ed2d061b773c136a7d4e2db9f05a9103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162369"
---
# <span data-ttu-id="79d02-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="79d02-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="79d02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d02-102">SYNOPSIS</span></span>
<span data-ttu-id="79d02-103">Erstellen eines Speicherobjekts für die Erweiterung</span><span class="sxs-lookup"><span data-stu-id="79d02-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="79d02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79d02-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="79d02-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79d02-105">DESCRIPTION</span></span>
<span data-ttu-id="79d02-106">Erstellen eines Speicherobjekts für die Erweiterung</span><span class="sxs-lookup"><span data-stu-id="79d02-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="79d02-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79d02-107">EXAMPLES</span></span>

### <span data-ttu-id="79d02-108">Beispiel 1: Erstellen eines Erweiterungsobjekts für "Geneva"</span><span class="sxs-lookup"><span data-stu-id="79d02-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="79d02-109">Mit diesem Befehl wird ein Erweiterungsobjekt für "Geneva" erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="79d02-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="79d02-110">Weitere Details finden Sie unter "New-AzCloudService".</span><span class="sxs-lookup"><span data-stu-id="79d02-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="79d02-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79d02-111">PARAMETERS</span></span>

### <span data-ttu-id="79d02-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="79d02-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="79d02-113">Geben Sie explizit an, ob CRP automatisch ein Upgrade von "typeHandlerVersion" auf höhere Nebenversionen durchführen kann, sobald diese verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="79d02-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-114">-Name</span><span class="sxs-lookup"><span data-stu-id="79d02-114">-Name</span></span>
<span data-ttu-id="79d02-115">Name.</span><span class="sxs-lookup"><span data-stu-id="79d02-115">Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="79d02-116">-ProtectedSetting</span></span>
<span data-ttu-id="79d02-117">Geschützte Einstellungen für die Erweiterung, die verschlüsselt werden, bevor sie an die VM gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="79d02-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="79d02-118">-Publisher</span></span>
<span data-ttu-id="79d02-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="79d02-119">Publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="79d02-120">-RolesAppliedTo</span></span>
<span data-ttu-id="79d02-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="79d02-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-122">-Einstellung</span><span class="sxs-lookup"><span data-stu-id="79d02-122">-Setting</span></span>
<span data-ttu-id="79d02-123">Öffentliche Einstellungen für die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="79d02-123">Public settings for the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-124">-Type</span><span class="sxs-lookup"><span data-stu-id="79d02-124">-Type</span></span>
<span data-ttu-id="79d02-125">Geben Sie den Text ein.</span><span class="sxs-lookup"><span data-stu-id="79d02-125">Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="79d02-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="79d02-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="79d02-127">TypeHandlerVersion.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79d02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d02-128">CommonParameters</span></span>
<span data-ttu-id="79d02-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79d02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d02-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79d02-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d02-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79d02-131">INPUTS</span></span>

## <span data-ttu-id="79d02-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79d02-132">OUTPUTS</span></span>

### <span data-ttu-id="79d02-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="79d02-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="79d02-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="79d02-134">NOTES</span></span>

<span data-ttu-id="79d02-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="79d02-135">ALIASES</span></span>

## <span data-ttu-id="79d02-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="79d02-136">RELATED LINKS</span></span>

