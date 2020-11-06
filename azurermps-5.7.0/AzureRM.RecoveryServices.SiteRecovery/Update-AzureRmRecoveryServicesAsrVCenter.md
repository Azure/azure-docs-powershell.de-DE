---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478281"
---
# <span data-ttu-id="47e7c-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="47e7c-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="47e7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="47e7c-103">Aktualisieren Sie die Ermittlungs Details für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="47e7c-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47e7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47e7c-104">SYNTAX</span></span>

### <span data-ttu-id="47e7c-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="47e7c-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e7c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="47e7c-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e7c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47e7c-107">DESCRIPTION</span></span>
<span data-ttu-id="47e7c-108">Das Cmdlet **Update-AzureRmRecoveryServicesAsrvCenter** ist eine Aktualisierungs Ermittlungs Details für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="47e7c-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="47e7c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="47e7c-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47e7c-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="47e7c-111">Aktualisieren Sie die Ermittlungs Details für ein registriertes vCenter.</span><span class="sxs-lookup"><span data-stu-id="47e7c-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="47e7c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="47e7c-112">PARAMETERS</span></span>

### <span data-ttu-id="47e7c-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="47e7c-113">-Account</span></span>
<span data-ttu-id="47e7c-114">vCenter-Anmeldeinformationen-Konto.</span><span class="sxs-lookup"><span data-stu-id="47e7c-114">vCenter login credentials account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e7c-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47e7c-115">-Confirm</span></span>
<span data-ttu-id="47e7c-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47e7c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e7c-117">-DefaultProfile</span></span>
<span data-ttu-id="47e7c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47e7c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47e7c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="47e7c-119">-InputObject</span></span>
<span data-ttu-id="47e7c-120">Das vCenter Server-Objekt, für das die Ermittlungs Details aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47e7c-120">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="47e7c-121">-Port</span><span class="sxs-lookup"><span data-stu-id="47e7c-121">-Port</span></span>
<span data-ttu-id="47e7c-122">Der TCP-Port auf dem vCenter Server, der für die Erkennung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47e7c-122">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47e7c-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="47e7c-123">-ResourceId</span></span>
<span data-ttu-id="47e7c-124">Gibt die Resourcen-Nr von vCenter an.</span><span class="sxs-lookup"><span data-stu-id="47e7c-124">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="47e7c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e7c-125">-WhatIf</span></span>
<span data-ttu-id="47e7c-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47e7c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47e7c-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47e7c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e7c-128">CommonParameters</span></span>
<span data-ttu-id="47e7c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e7c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47e7c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e7c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47e7c-131">INPUTS</span></span>

### <span data-ttu-id="47e7c-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="47e7c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="47e7c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47e7c-133">OUTPUTS</span></span>

### <span data-ttu-id="47e7c-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="47e7c-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="47e7c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="47e7c-135">NOTES</span></span>

## <span data-ttu-id="47e7c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47e7c-136">RELATED LINKS</span></span>
