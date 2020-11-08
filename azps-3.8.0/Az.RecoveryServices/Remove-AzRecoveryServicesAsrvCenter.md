---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 775a8694df895601d953a1efd68b7a4cba57a830
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997327"
---
# <span data-ttu-id="66739-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="66739-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="66739-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66739-102">SYNOPSIS</span></span>
<span data-ttu-id="66739-103">Entfernt den vCenter Server aus dem ASR-Fabric und beendet die Ermittlung virtueller Computer vom vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="66739-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="66739-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66739-104">SYNTAX</span></span>

### <span data-ttu-id="66739-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="66739-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66739-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="66739-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66739-107">ByName</span><span class="sxs-lookup"><span data-stu-id="66739-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66739-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66739-108">DESCRIPTION</span></span>
<span data-ttu-id="66739-109">Mit dem Cmdlet **Remove-AzRecoveryServicesAsrvCenter** wird der vCenter Server aus dem ASR-Fabric entfernt und die Ermittlung virtueller Computer vom vCenter Server beendet.</span><span class="sxs-lookup"><span data-stu-id="66739-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="66739-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66739-110">EXAMPLES</span></span>

### <span data-ttu-id="66739-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="66739-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="66739-112">Entfernt den vCenter Server aus dem ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="66739-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="66739-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="66739-113">PARAMETERS</span></span>

### <span data-ttu-id="66739-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66739-114">-DefaultProfile</span></span>
<span data-ttu-id="66739-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66739-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66739-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="66739-116">-Fabric</span></span>
<span data-ttu-id="66739-117">ASR-Fabric-Objekt, das den Konfigurations Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="66739-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66739-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="66739-118">-InputObject</span></span>
<span data-ttu-id="66739-119">ASR-vCenter-Objekt, das den zu entfernenden vCenter Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="66739-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66739-120">-Name</span><span class="sxs-lookup"><span data-stu-id="66739-120">-Name</span></span>
<span data-ttu-id="66739-121">Der Name des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="66739-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66739-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="66739-122">-ResourceId</span></span>
<span data-ttu-id="66739-123">Gibt die zu entfernende ressourcensource-zu vCenter</span><span class="sxs-lookup"><span data-stu-id="66739-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66739-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="66739-124">-Confirm</span></span>
<span data-ttu-id="66739-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="66739-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66739-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66739-126">-WhatIf</span></span>
<span data-ttu-id="66739-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66739-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66739-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66739-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66739-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66739-129">CommonParameters</span></span>
<span data-ttu-id="66739-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66739-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66739-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66739-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66739-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66739-132">INPUTS</span></span>

### <span data-ttu-id="66739-133">System. String</span><span class="sxs-lookup"><span data-stu-id="66739-133">System.String</span></span>

### <span data-ttu-id="66739-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="66739-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="66739-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="66739-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="66739-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66739-136">OUTPUTS</span></span>

### <span data-ttu-id="66739-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="66739-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="66739-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="66739-138">NOTES</span></span>

## <span data-ttu-id="66739-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66739-139">RELATED LINKS</span></span>
