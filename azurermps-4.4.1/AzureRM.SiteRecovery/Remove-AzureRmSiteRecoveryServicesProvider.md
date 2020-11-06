---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481510"
---
# <span data-ttu-id="ce4ba-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ce4ba-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="ce4ba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce4ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4ba-103">Entfernt einen Azure Site Recovery Services-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce4ba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce4ba-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce4ba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce4ba-105">DESCRIPTION</span></span>
<span data-ttu-id="ce4ba-106">Mit dem Cmdlet **Remove-AzureRmSiteRecoveryServicesProvider** wird ein Azure Site Recovery Services-Anbieter aus dem Tresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="ce4ba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce4ba-107">EXAMPLES</span></span>

## <span data-ttu-id="ce4ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce4ba-108">PARAMETERS</span></span>

### <span data-ttu-id="ce4ba-109">-Force</span><span class="sxs-lookup"><span data-stu-id="ce4ba-109">-Force</span></span>
<span data-ttu-id="ce4ba-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ce4ba-111">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ce4ba-111">-ServicesProvider</span></span>
<span data-ttu-id="ce4ba-112">Gibt das Dienstanbieterobjekt an.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4ba-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce4ba-113">-Confirm</span></span>
<span data-ttu-id="ce4ba-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce4ba-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce4ba-115">-WhatIf</span></span>
<span data-ttu-id="ce4ba-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ce4ba-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce4ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4ba-118">-DefaultProfile</span></span>
<span data-ttu-id="ce4ba-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce4ba-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4ba-120">CommonParameters</span></span>
<span data-ttu-id="ce4ba-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4ba-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce4ba-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4ba-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce4ba-123">INPUTS</span></span>

### <span data-ttu-id="ce4ba-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ce4ba-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="ce4ba-125">Der Parameter "ServicesProvider" akzeptiert den Wert vom Typ "ASRRecoveryServicesProvider" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce4ba-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="ce4ba-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce4ba-126">OUTPUTS</span></span>

### <span data-ttu-id="ce4ba-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ce4ba-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ce4ba-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce4ba-128">NOTES</span></span>

## <span data-ttu-id="ce4ba-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce4ba-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce4ba-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ce4ba-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="ce4ba-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="ce4ba-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
