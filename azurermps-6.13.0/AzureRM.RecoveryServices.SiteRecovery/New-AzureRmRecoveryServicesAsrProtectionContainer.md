---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: b551e89a800c70f1321a1f58cf4d5eae39fe69e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475969"
---
# <span data-ttu-id="b622e-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b622e-101">New-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="b622e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b622e-102">SYNOPSIS</span></span>
<span data-ttu-id="b622e-103">Erstellt einen Azure Site Recovery Protection-Container innerhalb des angegebenen Fabrics.</span><span class="sxs-lookup"><span data-stu-id="b622e-103">Creates an Azure Site Recovery Protection Container within the specified fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b622e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b622e-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -InputObject <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b622e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b622e-105">DESCRIPTION</span></span>
<span data-ttu-id="b622e-106">Das New-AzureRmRecoveryServicesAsrProtectionContainer-Cmdlet erstellt einen Schutz Container unter dem angegebenen Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="b622e-106">The New-AzureRmRecoveryServicesAsrProtectionContainer cmdlet creates a Protection Container under the specified Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="b622e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b622e-107">EXAMPLES</span></span>

### <span data-ttu-id="b622e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b622e-108">Example 1</span></span>
```
PS C:\> $job = New-AzureRmRecoveryServicesAsrProtectionContainer -Name xyz -Fabric $fabric
PS C:\> Get-ASRJob -name $job.id
```

<span data-ttu-id="b622e-109">Startet die Erstellung des Schutz Containers mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b622e-109">Starts the creation of the protection container with the specified parameters, and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b622e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b622e-110">PARAMETERS</span></span>

### <span data-ttu-id="b622e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b622e-111">-DefaultProfile</span></span>
<span data-ttu-id="b622e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b622e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b622e-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b622e-113">-InputObject</span></span>
<span data-ttu-id="b622e-114">Erstellt den Replikations Schutzcontainer in angegebene-Eingabeobjekt (Azure Fabric).</span><span class="sxs-lookup"><span data-stu-id="b622e-114">Creates the replication protection container in specifed input Object (Azure Fabric).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b622e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b622e-115">-Name</span></span>
<span data-ttu-id="b622e-116">Der Name des Schutz Containers.</span><span class="sxs-lookup"><span data-stu-id="b622e-116">Name of the protection container.</span></span>

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

### <span data-ttu-id="b622e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b622e-117">-Confirm</span></span>
<span data-ttu-id="b622e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b622e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b622e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b622e-119">-WhatIf</span></span>
<span data-ttu-id="b622e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b622e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b622e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b622e-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b622e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b622e-122">CommonParameters</span></span>
<span data-ttu-id="b622e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b622e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b622e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b622e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b622e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b622e-125">INPUTS</span></span>

### <span data-ttu-id="b622e-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b622e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b622e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b622e-127">OUTPUTS</span></span>

### <span data-ttu-id="b622e-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b622e-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b622e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="b622e-129">NOTES</span></span>

## <span data-ttu-id="b622e-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b622e-130">RELATED LINKS</span></span>
