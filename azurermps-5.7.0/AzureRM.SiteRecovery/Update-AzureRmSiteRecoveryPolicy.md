---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 313E7444-2EB4-4B91-9E56-5730CB006046
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: b4e6cff174f0bb623145a4b364b2c22297530c51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476541"
---
# <span data-ttu-id="293dd-101">Update-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="293dd-101">Update-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="293dd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="293dd-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="293dd-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="293dd-103">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="293dd-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="293dd-104">DESCRIPTION</span></span>

## <span data-ttu-id="293dd-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="293dd-105">EXAMPLES</span></span>

## <span data-ttu-id="293dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="293dd-106">PARAMETERS</span></span>

### <span data-ttu-id="293dd-107">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="293dd-107">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-108">-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="293dd-108">-Authentication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-109">-Komprimierung</span><span class="sxs-lookup"><span data-stu-id="293dd-109">-Compression</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293dd-110">-DefaultProfile</span></span>
<span data-ttu-id="293dd-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="293dd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="293dd-112">-Verschlüsselung</span><span class="sxs-lookup"><span data-stu-id="293dd-112">-Encryption</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-113">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="293dd-113">-Policy</span></span>
```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-114">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="293dd-114">-RecoveryAzureStorageAccountId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-115">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="293dd-115">-RecoveryPoints</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-116">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="293dd-116">-ReplicaDeletion</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-117">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="293dd-117">-ReplicationFrequencyInSeconds</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-118">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="293dd-118">-ReplicationMethod</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-119">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="293dd-119">-ReplicationPort</span></span>
```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-120">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="293dd-120">-ReplicationStartTime</span></span>
```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="293dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293dd-121">CommonParameters</span></span>
<span data-ttu-id="293dd-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="293dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293dd-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="293dd-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293dd-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="293dd-124">INPUTS</span></span>

### <span data-ttu-id="293dd-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="293dd-125">ASRPolicy</span></span>
<span data-ttu-id="293dd-126">Der Parameter "Richtlinie" akzeptiert den Wert vom Typ "ASRPolicy" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="293dd-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="293dd-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="293dd-127">OUTPUTS</span></span>

## <span data-ttu-id="293dd-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="293dd-128">NOTES</span></span>

## <span data-ttu-id="293dd-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="293dd-129">RELATED LINKS</span></span>

