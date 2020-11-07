---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 8e2b563563ca50e0fdf6913a9e9999e1a642ff9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664425"
---
# <span data-ttu-id="e1ab6-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e1ab6-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="e1ab6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ab6-103">Ruft Speicher Klassifizierungen bei der Websitewiederherstellung ab.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ab6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ab6-104">SYNTAX</span></span>

### <span data-ttu-id="e1ab6-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1ab6-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1ab6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e1ab6-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ab6-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e1ab6-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ab6-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="e1ab6-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ab6-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="e1ab6-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ab6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1ab6-110">DESCRIPTION</span></span>
<span data-ttu-id="e1ab6-111">Das Cmdlet " **Get-AzureRmSiteRecoveryStorageClassification** " ruft Speicher Klassifizierungen in Azure Site Recovery ab.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="e1ab6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1ab6-112">EXAMPLES</span></span>

## <span data-ttu-id="e1ab6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1ab6-113">PARAMETERS</span></span>

### <span data-ttu-id="e1ab6-114">-Stoff</span><span class="sxs-lookup"><span data-stu-id="e1ab6-114">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e1ab6-115">-FriendlyName</span></span>
<span data-ttu-id="e1ab6-116">Gibt den Anzeigenamen der speicherklassifizierung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-116">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e1ab6-117">-Name</span></span>
<span data-ttu-id="e1ab6-118">Gibt den Namen der speicherklassifizierung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-118">Specifies the name of the storage classification that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e1ab6-119">-Server</span><span class="sxs-lookup"><span data-stu-id="e1ab6-119">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ab6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ab6-120">-DefaultProfile</span></span>
<span data-ttu-id="e1ab6-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1ab6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ab6-122">CommonParameters</span></span>
<span data-ttu-id="e1ab6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ab6-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ab6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ab6-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1ab6-125">INPUTS</span></span>

### <span data-ttu-id="e1ab6-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e1ab6-126">ASRFabric</span></span>
<span data-ttu-id="e1ab6-127">Der Parameter "Fabric" akzeptiert den Wert vom Typ "ASRFabric" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="e1ab6-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="e1ab6-128">ASRServer</span></span>
<span data-ttu-id="e1ab6-129">Der Parameter "Server" akzeptiert den Wert vom Typ "ASRServer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e1ab6-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="e1ab6-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1ab6-130">OUTPUTS</span></span>

### <span data-ttu-id="e1ab6-131">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="e1ab6-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="e1ab6-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1ab6-132">NOTES</span></span>

## <span data-ttu-id="e1ab6-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1ab6-133">RELATED LINKS</span></span>

