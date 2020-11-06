---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: eaa357e6dd216b62a2c8e8f1cd78ff15387be57a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482830"
---
# <span data-ttu-id="8b894-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="8b894-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="8b894-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b894-102">SYNOPSIS</span></span>
<span data-ttu-id="8b894-103">Entfernt den vCenter Server aus dem ASR-Fabric und beendet die Ermittlung virtueller Computer vom vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="8b894-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b894-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b894-104">SYNTAX</span></span>

### <span data-ttu-id="8b894-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b894-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b894-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b894-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b894-107">ByName</span><span class="sxs-lookup"><span data-stu-id="8b894-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b894-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b894-108">DESCRIPTION</span></span>
<span data-ttu-id="8b894-109">Mit dem Cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** wird der vCenter Server aus dem ASR-Fabric entfernt und die Ermittlung virtueller Computer vom vCenter Server beendet.</span><span class="sxs-lookup"><span data-stu-id="8b894-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="8b894-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b894-110">EXAMPLES</span></span>

### <span data-ttu-id="8b894-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b894-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="8b894-112">Entfernt den vCenter Server aus dem ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="8b894-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="8b894-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b894-113">PARAMETERS</span></span>

### <span data-ttu-id="8b894-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b894-114">-Confirm</span></span>
<span data-ttu-id="8b894-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b894-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b894-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b894-116">-DefaultProfile</span></span>
<span data-ttu-id="8b894-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b894-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b894-118">-Stoff</span><span class="sxs-lookup"><span data-stu-id="8b894-118">-Fabric</span></span>
<span data-ttu-id="8b894-119">ASR-Fabric-Objekt, das den Konfigurations Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b894-119">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b894-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b894-120">-InputObject</span></span>
<span data-ttu-id="8b894-121">ASR-vCenter-Objekt, das den zu entfernenden vCenter Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b894-121">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b894-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8b894-122">-Name</span></span>
<span data-ttu-id="8b894-123">Der Name des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="8b894-123">Name of the vCenter Server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b894-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8b894-124">-ResourceId</span></span>
<span data-ttu-id="8b894-125">Gibt die zu entfernende ressourcensource-zu vCenter</span><span class="sxs-lookup"><span data-stu-id="8b894-125">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b894-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b894-126">-WhatIf</span></span>
<span data-ttu-id="8b894-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b894-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b894-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b894-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b894-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b894-129">CommonParameters</span></span>
<span data-ttu-id="8b894-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b894-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b894-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b894-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b894-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b894-132">INPUTS</span></span>

### <span data-ttu-id="8b894-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="8b894-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="8b894-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b894-134">OUTPUTS</span></span>

### <span data-ttu-id="8b894-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="8b894-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8b894-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b894-136">NOTES</span></span>

## <span data-ttu-id="8b894-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b894-137">RELATED LINKS</span></span>
