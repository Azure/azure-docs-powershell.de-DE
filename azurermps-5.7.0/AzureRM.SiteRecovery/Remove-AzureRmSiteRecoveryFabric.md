---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 43d9603a5938ecef084191ebe77888a5f1769673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502365"
---
# <span data-ttu-id="48120-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="48120-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="48120-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48120-102">SYNOPSIS</span></span>
<span data-ttu-id="48120-103">Entfernt eine Azure Site-Wiederherstellungsstruktur.</span><span class="sxs-lookup"><span data-stu-id="48120-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48120-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48120-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48120-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48120-105">DESCRIPTION</span></span>
<span data-ttu-id="48120-106">Das Cmdlet **Remove-AzureRmSiteRecoveryFabric** entfernt ein Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="48120-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="48120-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48120-107">EXAMPLES</span></span>

## <span data-ttu-id="48120-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="48120-108">PARAMETERS</span></span>

### <span data-ttu-id="48120-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48120-109">-DefaultProfile</span></span>
<span data-ttu-id="48120-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48120-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48120-111">-Stoff</span><span class="sxs-lookup"><span data-stu-id="48120-111">-Fabric</span></span>
<span data-ttu-id="48120-112">Gibt das Fabric-Objekt für Azure Site Recovery an.</span><span class="sxs-lookup"><span data-stu-id="48120-112">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48120-113">-Force</span><span class="sxs-lookup"><span data-stu-id="48120-113">-Force</span></span>
<span data-ttu-id="48120-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="48120-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48120-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48120-115">-Confirm</span></span>
<span data-ttu-id="48120-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48120-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48120-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48120-117">-WhatIf</span></span>
<span data-ttu-id="48120-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48120-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="48120-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48120-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48120-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48120-120">CommonParameters</span></span>
<span data-ttu-id="48120-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48120-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48120-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48120-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48120-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48120-123">INPUTS</span></span>

### <span data-ttu-id="48120-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="48120-124">ASRFabric</span></span>
<span data-ttu-id="48120-125">Der Parameter "Fabric" akzeptiert den Wert vom Typ "ASRFabric" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="48120-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="48120-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48120-126">OUTPUTS</span></span>

### <span data-ttu-id="48120-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="48120-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="48120-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="48120-128">NOTES</span></span>

## <span data-ttu-id="48120-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48120-129">RELATED LINKS</span></span>

[<span data-ttu-id="48120-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="48120-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="48120-131">Neu – AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="48120-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
