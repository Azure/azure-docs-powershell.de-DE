---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4CC5E6A8-B51A-49ED-BB93-FE63F1500780
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryNetwork.md
ms.openlocfilehash: 83410371d517bbd90a0b302d258ff25325e06cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481525"
---
# <span data-ttu-id="46b47-101">Get-AzureRmSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="46b47-101">Get-AzureRmSiteRecoveryNetwork</span></span>

## <span data-ttu-id="46b47-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46b47-102">SYNOPSIS</span></span>
<span data-ttu-id="46b47-103">Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="46b47-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b47-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46b47-104">SYNTAX</span></span>

### <span data-ttu-id="46b47-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="46b47-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryNetwork [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46b47-106">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="46b47-106">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46b47-107">ByNameLegacy</span><span class="sxs-lookup"><span data-stu-id="46b47-107">ByNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46b47-108">ByFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="46b47-108">ByFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Server <ASRServer> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46b47-109">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="46b47-109">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46b47-110">ByName</span><span class="sxs-lookup"><span data-stu-id="46b47-110">ByName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46b47-111">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="46b47-111">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46b47-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46b47-112">DESCRIPTION</span></span>
<span data-ttu-id="46b47-113">Das Cmdlet " **Get-AzureRmSiteRecoveryNetwork** " Ruft Informationen zu Azure Site Recovery Networks für das aktuelle Azure Site Recovery Vault ab.</span><span class="sxs-lookup"><span data-stu-id="46b47-113">The **Get-AzureRmSiteRecoveryNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="46b47-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46b47-114">EXAMPLES</span></span>

## <span data-ttu-id="46b47-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="46b47-115">PARAMETERS</span></span>

### <span data-ttu-id="46b47-116">-Stoff</span><span class="sxs-lookup"><span data-stu-id="46b47-116">-Fabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject, ByName, ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46b47-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="46b47-117">-FriendlyName</span></span>
<span data-ttu-id="46b47-118">Gibt den Anzeigenamen des virtuellen Computernetzwerks an.</span><span class="sxs-lookup"><span data-stu-id="46b47-118">Specifies the friendly name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46b47-119">-Name</span><span class="sxs-lookup"><span data-stu-id="46b47-119">-Name</span></span>
<span data-ttu-id="46b47-120">Gibt den Namen des Netzwerks des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="46b47-120">Specifies the name of the virtual machine network.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46b47-121">-Server</span><span class="sxs-lookup"><span data-stu-id="46b47-121">-Server</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByServerObject, ByNameLegacy, ByFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46b47-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b47-122">-DefaultProfile</span></span>
<span data-ttu-id="46b47-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46b47-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46b47-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b47-124">CommonParameters</span></span>
<span data-ttu-id="46b47-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b47-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b47-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b47-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b47-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46b47-127">INPUTS</span></span>

### <span data-ttu-id="46b47-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="46b47-128">ASRFabric</span></span>
<span data-ttu-id="46b47-129">Der Parameter "Fabric" akzeptiert den Wert vom Typ "ASRFabric" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46b47-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="46b47-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="46b47-130">String</span></span>
<span data-ttu-id="46b47-131">Der Parameter "FriendlyName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46b47-131">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="46b47-132">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="46b47-132">String</span></span>
<span data-ttu-id="46b47-133">Der Parameter "FriendlyName" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46b47-133">Parameter 'FriendlyName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="46b47-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="46b47-134">String</span></span>
<span data-ttu-id="46b47-135">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46b47-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="46b47-136">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="46b47-136">String</span></span>
<span data-ttu-id="46b47-137">Der Parameter "Name" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46b47-137">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="46b47-138">ASRServer</span><span class="sxs-lookup"><span data-stu-id="46b47-138">ASRServer</span></span>
<span data-ttu-id="46b47-139">Der Parameter "Server" akzeptiert den Wert vom Typ "ASRServer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46b47-139">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="46b47-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46b47-140">OUTPUTS</span></span>

### <span data-ttu-id="46b47-141">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRNetwork]</span><span class="sxs-lookup"><span data-stu-id="46b47-141">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRNetwork]</span></span>

## <span data-ttu-id="46b47-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="46b47-142">NOTES</span></span>

## <span data-ttu-id="46b47-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46b47-143">RELATED LINKS</span></span>

