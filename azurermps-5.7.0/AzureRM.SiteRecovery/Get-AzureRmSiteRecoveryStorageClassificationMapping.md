---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D19488C1-9E87-4F1A-94E3-8AFDE6AFC982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: e04f5b71fe0cc5d6872c3bdf9cd18790f4e09f7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664179"
---
# <span data-ttu-id="4f553-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="4f553-101">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="4f553-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f553-102">SYNOPSIS</span></span>
<span data-ttu-id="4f553-103">Ruft eine Speicher Klassifikations Zuordnung in der Websitewiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="4f553-103">Gets a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f553-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f553-104">SYNTAX</span></span>

### <span data-ttu-id="4f553-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f553-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f553-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4f553-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassificationMapping -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f553-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f553-107">DESCRIPTION</span></span>
<span data-ttu-id="4f553-108">Das Cmdlet " **Get-AzureRmSiteRecoveryStorageClassificationMapping** " Ruft eine Speicher Klassifikations Zuordnung in Azure Site Recovery ab.</span><span class="sxs-lookup"><span data-stu-id="4f553-108">The **Get-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet gets a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="4f553-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f553-109">EXAMPLES</span></span>

## <span data-ttu-id="4f553-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f553-110">PARAMETERS</span></span>

### <span data-ttu-id="4f553-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f553-111">-DefaultProfile</span></span>
<span data-ttu-id="4f553-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f553-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f553-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4f553-113">-Name</span></span>
<span data-ttu-id="4f553-114">Gibt den Namen der Speicher Klassifikations Zuordnung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4f553-114">Specifies the name of the storage classification mapping that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4f553-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f553-115">CommonParameters</span></span>
<span data-ttu-id="4f553-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f553-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f553-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f553-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f553-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f553-118">INPUTS</span></span>

### <span data-ttu-id="4f553-119">Keine</span><span class="sxs-lookup"><span data-stu-id="4f553-119">None</span></span>
<span data-ttu-id="4f553-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4f553-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f553-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f553-121">OUTPUTS</span></span>

### <span data-ttu-id="4f553-122">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassificationMapping]</span><span class="sxs-lookup"><span data-stu-id="4f553-122">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping]</span></span>

## <span data-ttu-id="4f553-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f553-123">NOTES</span></span>

## <span data-ttu-id="4f553-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f553-124">RELATED LINKS</span></span>

[<span data-ttu-id="4f553-125">Neu – AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="4f553-125">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="4f553-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="4f553-126">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
