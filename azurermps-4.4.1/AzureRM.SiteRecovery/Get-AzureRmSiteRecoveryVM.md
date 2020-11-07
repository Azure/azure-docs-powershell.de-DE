---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662891"
---
# <span data-ttu-id="3cb1f-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3cb1f-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="3cb1f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb1f-103">Ruft Informationen zu den von der Websitewiederherstellung verwalteten virtuellen Computern ab.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cb1f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cb1f-104">SYNTAX</span></span>

### <span data-ttu-id="3cb1f-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cb1f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cb1f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3cb1f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cb1f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3cb1f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cb1f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cb1f-108">DESCRIPTION</span></span>
<span data-ttu-id="3cb1f-109">Das Cmdlet " **Get-AzureRmSiteRecoveryVM** " Ruft Informationen zu virtuellen Computern ab, die in Azure Site Recovery verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="3cb1f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cb1f-110">EXAMPLES</span></span>

## <span data-ttu-id="3cb1f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cb1f-111">PARAMETERS</span></span>

### <span data-ttu-id="3cb1f-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3cb1f-112">-FriendlyName</span></span>
<span data-ttu-id="3cb1f-113">Gibt den Anzeigenamen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-113">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb1f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="3cb1f-114">-Name</span></span>
<span data-ttu-id="3cb1f-115">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb1f-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3cb1f-116">-ProtectionContainer</span></span>
<span data-ttu-id="3cb1f-117">Gibt das Containerobjekt für den Website Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb1f-118">-DefaultProfile</span></span>
<span data-ttu-id="3cb1f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cb1f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb1f-120">CommonParameters</span></span>
<span data-ttu-id="3cb1f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb1f-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb1f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb1f-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cb1f-123">INPUTS</span></span>

### <span data-ttu-id="3cb1f-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3cb1f-124">ASRProtectionContainer</span></span>
<span data-ttu-id="3cb1f-125">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="3cb1f-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3cb1f-126">ASRProtectionContainer</span></span>
<span data-ttu-id="3cb1f-127">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3cb1f-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="3cb1f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cb1f-128">OUTPUTS</span></span>

### <span data-ttu-id="3cb1f-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="3cb1f-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="3cb1f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cb1f-130">NOTES</span></span>

## <span data-ttu-id="3cb1f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cb1f-131">RELATED LINKS</span></span>

[<span data-ttu-id="3cb1f-132">Satz-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3cb1f-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
