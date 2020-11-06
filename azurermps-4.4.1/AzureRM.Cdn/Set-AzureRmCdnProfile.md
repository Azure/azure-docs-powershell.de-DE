---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: 8e294b457d93c5e9aeb9f8391fccdedc3ccfd778
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497861"
---
# <span data-ttu-id="6c8f6-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="6c8f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6c8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c8f6-103">Aktualisiert ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c8f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c8f6-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c8f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c8f6-106">Das Cmdlet " **Satz-AzureRmCdnProfile** " aktualisiert ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="6c8f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c8f6-107">EXAMPLES</span></span>

## <span data-ttu-id="6c8f6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c8f6-108">PARAMETERS</span></span>

### <span data-ttu-id="6c8f6-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-109">-CdnProfile</span></span>
<span data-ttu-id="6c8f6-110">Gibt das Profil an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c8f6-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c8f6-111">-Confirm</span></span>
<span data-ttu-id="6c8f6-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c8f6-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c8f6-113">-WhatIf</span></span>
<span data-ttu-id="6c8f6-114">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c8f6-115">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c8f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-116">-DefaultProfile</span></span>
<span data-ttu-id="6c8f6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c8f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c8f6-118">CommonParameters</span></span>
<span data-ttu-id="6c8f6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c8f6-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c8f6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c8f6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6c8f6-121">INPUTS</span></span>

### <span data-ttu-id="6c8f6-122">PSProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-122">PSProfile</span></span>
<span data-ttu-id="6c8f6-123">Der Parameter "CdnProfile" akzeptiert den Wert vom Typ "PSProfile" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6c8f6-123">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="6c8f6-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6c8f6-124">OUTPUTS</span></span>

### <span data-ttu-id="6c8f6-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="6c8f6-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="6c8f6-126">NOTES</span></span>

## <span data-ttu-id="6c8f6-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6c8f6-127">RELATED LINKS</span></span>

[<span data-ttu-id="6c8f6-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="6c8f6-129">Neu – AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="6c8f6-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="6c8f6-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


