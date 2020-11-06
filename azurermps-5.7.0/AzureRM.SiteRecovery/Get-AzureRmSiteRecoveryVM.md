---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502389"
---
# <span data-ttu-id="3f472-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3f472-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="3f472-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f472-102">SYNOPSIS</span></span>
<span data-ttu-id="3f472-103">Ruft Informationen zu den von der Websitewiederherstellung verwalteten virtuellen Computern ab.</span><span class="sxs-lookup"><span data-stu-id="3f472-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f472-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f472-104">SYNTAX</span></span>

### <span data-ttu-id="3f472-105">ByObject (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f472-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f472-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3f472-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f472-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f472-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f472-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f472-108">DESCRIPTION</span></span>
<span data-ttu-id="3f472-109">Das Cmdlet " **Get-AzureRmSiteRecoveryVM** " Ruft Informationen zu virtuellen Computern ab, die in Azure Site Recovery verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3f472-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="3f472-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f472-110">EXAMPLES</span></span>

## <span data-ttu-id="3f472-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f472-111">PARAMETERS</span></span>

### <span data-ttu-id="3f472-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f472-112">-DefaultProfile</span></span>
<span data-ttu-id="3f472-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f472-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f472-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3f472-114">-FriendlyName</span></span>
<span data-ttu-id="3f472-115">Gibt den Anzeigenamen des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="3f472-115">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f472-116">-Name</span><span class="sxs-lookup"><span data-stu-id="3f472-116">-Name</span></span>
<span data-ttu-id="3f472-117">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="3f472-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f472-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3f472-118">-ProtectionContainer</span></span>
<span data-ttu-id="3f472-119">Gibt das Containerobjekt für den Website Wiederherstellungs Schutz an.</span><span class="sxs-lookup"><span data-stu-id="3f472-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f472-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f472-120">CommonParameters</span></span>
<span data-ttu-id="3f472-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f472-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f472-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f472-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f472-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f472-123">INPUTS</span></span>

### <span data-ttu-id="3f472-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3f472-124">ASRProtectionContainer</span></span>
<span data-ttu-id="3f472-125">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f472-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="3f472-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3f472-126">ASRProtectionContainer</span></span>
<span data-ttu-id="3f472-127">Der Parameter "ProtectionContainer" akzeptiert den Wert vom Typ "ASRProtectionContainer" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3f472-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="3f472-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f472-128">OUTPUTS</span></span>

### <span data-ttu-id="3f472-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="3f472-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="3f472-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f472-130">NOTES</span></span>

## <span data-ttu-id="3f472-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f472-131">RELATED LINKS</span></span>

[<span data-ttu-id="3f472-132">Satz-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3f472-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
