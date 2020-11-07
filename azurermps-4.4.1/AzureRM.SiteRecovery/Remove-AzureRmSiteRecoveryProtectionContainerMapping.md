---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: a0de6cc5594b019275cb14785cbae3b969d44301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662888"
---
# <span data-ttu-id="8be9e-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8be9e-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="8be9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8be9e-102">SYNOPSIS</span></span>
<span data-ttu-id="8be9e-103">Entfernt eine Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8be9e-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be9e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8be9e-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be9e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8be9e-105">DESCRIPTION</span></span>
<span data-ttu-id="8be9e-106">Das Cmdlet **Remove-AzureRmSiteRecoveryProtectionContainerMapping** entfernt eine Azure Site Recovery Protection-Container Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="8be9e-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="8be9e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8be9e-107">EXAMPLES</span></span>

## <span data-ttu-id="8be9e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8be9e-108">PARAMETERS</span></span>

### <span data-ttu-id="8be9e-109">-Force</span><span class="sxs-lookup"><span data-stu-id="8be9e-109">-Force</span></span>
<span data-ttu-id="8be9e-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8be9e-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be9e-111">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8be9e-111">-ProtectionContainerMapping</span></span>
<span data-ttu-id="8be9e-112">Gibt das Azure Site Recovery Protection Container-Zuordnungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="8be9e-112">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8be9e-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8be9e-113">-Confirm</span></span>
<span data-ttu-id="8be9e-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8be9e-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be9e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be9e-115">-WhatIf</span></span>
<span data-ttu-id="8be9e-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8be9e-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8be9e-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8be9e-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be9e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be9e-118">-DefaultProfile</span></span>
<span data-ttu-id="8be9e-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8be9e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8be9e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be9e-120">CommonParameters</span></span>
<span data-ttu-id="8be9e-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be9e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be9e-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be9e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be9e-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8be9e-123">INPUTS</span></span>

### <span data-ttu-id="8be9e-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8be9e-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="8be9e-125">Der Parameter "ProtectionContainerMapping" akzeptiert den Wert vom Typ "ASRProtectionContainerMapping" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8be9e-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="8be9e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8be9e-126">OUTPUTS</span></span>

### <span data-ttu-id="8be9e-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8be9e-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8be9e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="8be9e-128">NOTES</span></span>

## <span data-ttu-id="8be9e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8be9e-129">RELATED LINKS</span></span>

[<span data-ttu-id="8be9e-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8be9e-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="8be9e-131">Neu – AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8be9e-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
