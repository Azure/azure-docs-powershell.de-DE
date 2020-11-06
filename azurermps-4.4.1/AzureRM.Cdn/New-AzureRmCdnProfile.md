---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500913"
---
# <span data-ttu-id="90c6c-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90c6c-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="90c6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="90c6c-103">Erstellt ein CDN-Profil.</span><span class="sxs-lookup"><span data-stu-id="90c6c-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90c6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90c6c-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90c6c-105">DESCRIPTION</span></span>
<span data-ttu-id="90c6c-106">Das Cmdlet **New-AzureRmCdnProfile** erstellt ein Azure Content Delivery Network (CDN)-Profil.</span><span class="sxs-lookup"><span data-stu-id="90c6c-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="90c6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90c6c-107">EXAMPLES</span></span>

## <span data-ttu-id="90c6c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="90c6c-108">PARAMETERS</span></span>

### <span data-ttu-id="90c6c-109">-Standort</span><span class="sxs-lookup"><span data-stu-id="90c6c-109">-Location</span></span>
<span data-ttu-id="90c6c-110">Gibt den Ressourcen Standort des Profils an.</span><span class="sxs-lookup"><span data-stu-id="90c6c-110">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c6c-111">-Profilname</span><span class="sxs-lookup"><span data-stu-id="90c6c-111">-ProfileName</span></span>
<span data-ttu-id="90c6c-112">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="90c6c-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c6c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c6c-113">-ResourceGroupName</span></span>
<span data-ttu-id="90c6c-114">Gibt den Namen der Ressourcengruppe an, zu der das Profil gehört.</span><span class="sxs-lookup"><span data-stu-id="90c6c-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c6c-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="90c6c-115">-Sku</span></span>
<span data-ttu-id="90c6c-116">Gibt die SKU des Profils an.</span><span class="sxs-lookup"><span data-stu-id="90c6c-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c6c-117">-Tags</span><span class="sxs-lookup"><span data-stu-id="90c6c-117">-Tags</span></span>
<span data-ttu-id="90c6c-118">Sepcifies eine Hashtabelle mit Tags, die diesem Profil zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="90c6c-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c6c-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90c6c-119">-Confirm</span></span>
<span data-ttu-id="90c6c-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90c6c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c6c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c6c-121">-WhatIf</span></span>
<span data-ttu-id="90c6c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90c6c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c6c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90c6c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c6c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c6c-124">-DefaultProfile</span></span>
<span data-ttu-id="90c6c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90c6c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90c6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c6c-126">CommonParameters</span></span>
<span data-ttu-id="90c6c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90c6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c6c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90c6c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c6c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90c6c-129">INPUTS</span></span>

## <span data-ttu-id="90c6c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90c6c-130">OUTPUTS</span></span>

### <span data-ttu-id="90c6c-131">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="90c6c-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="90c6c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="90c6c-132">NOTES</span></span>

## <span data-ttu-id="90c6c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90c6c-133">RELATED LINKS</span></span>

[<span data-ttu-id="90c6c-134">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90c6c-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="90c6c-135">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90c6c-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="90c6c-136">Satz-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="90c6c-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


