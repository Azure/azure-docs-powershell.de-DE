---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502917"
---
# <span data-ttu-id="f4598-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="f4598-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="f4598-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4598-102">SYNOPSIS</span></span>
<span data-ttu-id="f4598-103">Entfernt den vCenter Server aus dem ASR-Fabric und beendet die Ermittlung virtueller Computer vom vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="f4598-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4598-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4598-104">SYNTAX</span></span>

### <span data-ttu-id="f4598-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4598-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4598-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4598-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4598-107">ByName</span><span class="sxs-lookup"><span data-stu-id="f4598-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4598-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4598-108">DESCRIPTION</span></span>
<span data-ttu-id="f4598-109">Mit dem Cmdlet **Remove-AzureRmRecoveryServicesAsrvCenter** wird der vCenter Server aus dem ASR-Fabric entfernt und die Ermittlung virtueller Computer vom vCenter Server beendet.</span><span class="sxs-lookup"><span data-stu-id="f4598-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="f4598-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4598-110">EXAMPLES</span></span>

### <span data-ttu-id="f4598-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4598-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="f4598-112">Entfernt den vCenter Server aus dem ASR-Fabric.</span><span class="sxs-lookup"><span data-stu-id="f4598-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="f4598-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4598-113">PARAMETERS</span></span>

### <span data-ttu-id="f4598-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4598-114">-DefaultProfile</span></span>
<span data-ttu-id="f4598-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f4598-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4598-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="f4598-116">-Fabric</span></span>
<span data-ttu-id="f4598-117">ASR-Fabric-Objekt, das den Konfigurations Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4598-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="f4598-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4598-118">-InputObject</span></span>
<span data-ttu-id="f4598-119">ASR-vCenter-Objekt, das den zu entfernenden vCenter Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4598-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="f4598-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f4598-120">-Name</span></span>
<span data-ttu-id="f4598-121">Der Name des vCenter-Servers.</span><span class="sxs-lookup"><span data-stu-id="f4598-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="f4598-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f4598-122">-ResourceId</span></span>
<span data-ttu-id="f4598-123">Gibt die zu entfernende ressourcensource-zu vCenter</span><span class="sxs-lookup"><span data-stu-id="f4598-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="f4598-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4598-124">-Confirm</span></span>
<span data-ttu-id="f4598-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4598-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4598-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4598-126">-WhatIf</span></span>
<span data-ttu-id="f4598-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4598-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4598-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4598-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4598-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4598-129">CommonParameters</span></span>
<span data-ttu-id="f4598-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4598-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4598-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4598-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4598-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4598-132">INPUTS</span></span>

### <span data-ttu-id="f4598-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="f4598-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="f4598-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4598-134">OUTPUTS</span></span>

### <span data-ttu-id="f4598-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f4598-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f4598-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4598-136">NOTES</span></span>

## <span data-ttu-id="f4598-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4598-137">RELATED LINKS</span></span>
