---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664168"
---
# <span data-ttu-id="d7a0a-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d7a0a-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="d7a0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7a0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a0a-103">Entfernt eine Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7a0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7a0a-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7a0a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7a0a-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a0a-106">Das Cmdlet **Remove-AzureRmSiteRecoveryProtectionContainerMapping** entfernt eine Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="d7a0a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7a0a-107">EXAMPLES</span></span>

## <span data-ttu-id="d7a0a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7a0a-108">PARAMETERS</span></span>

### <span data-ttu-id="d7a0a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a0a-109">-DefaultProfile</span></span>
<span data-ttu-id="d7a0a-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7a0a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d7a0a-111">-Force</span></span>
<span data-ttu-id="d7a0a-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7a0a-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d7a0a-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="d7a0a-114">Gibt das Azure Site Recovery Protection Container-Zuordnungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7a0a-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d7a0a-115">-Confirm</span></span>
<span data-ttu-id="d7a0a-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a0a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a0a-117">-WhatIf</span></span>
<span data-ttu-id="d7a0a-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d7a0a-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a0a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a0a-120">CommonParameters</span></span>
<span data-ttu-id="d7a0a-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a0a-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a0a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a0a-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7a0a-123">INPUTS</span></span>

### <span data-ttu-id="d7a0a-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d7a0a-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="d7a0a-125">Der Parameter "ProtectionContainerMapping" akzeptiert den Wert vom Typ "ASRProtectionContainerMapping" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d7a0a-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="d7a0a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7a0a-126">OUTPUTS</span></span>

### <span data-ttu-id="d7a0a-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d7a0a-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d7a0a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7a0a-128">NOTES</span></span>

## <span data-ttu-id="d7a0a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7a0a-129">RELATED LINKS</span></span>

[<span data-ttu-id="d7a0a-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d7a0a-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="d7a0a-131">Neu – AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d7a0a-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
