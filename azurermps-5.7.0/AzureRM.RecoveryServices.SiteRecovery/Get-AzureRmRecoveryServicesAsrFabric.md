---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 92631a1a6c5d27953777efe2b6ea158f59da8fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478310"
---
# <span data-ttu-id="06021-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="06021-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="06021-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06021-102">SYNOPSIS</span></span>
<span data-ttu-id="06021-103">Abrufen der Details eines Azure Site Recovery-Fabrics</span><span class="sxs-lookup"><span data-stu-id="06021-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06021-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06021-104">SYNTAX</span></span>

### <span data-ttu-id="06021-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="06021-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06021-106">ByName</span><span class="sxs-lookup"><span data-stu-id="06021-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06021-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="06021-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06021-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06021-108">DESCRIPTION</span></span>
<span data-ttu-id="06021-109">Das Cmdlet " **Get-AzureRmRecoveryServicesAsrFabric** " Ruft die Eigenschaften eines angegebenen Azure Site Recovery-Fabrics oder aller Azure Site Recovery-Fabrics in einem Recovery Service Vault ab.</span><span class="sxs-lookup"><span data-stu-id="06021-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="06021-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06021-110">EXAMPLES</span></span>

### <span data-ttu-id="06021-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06021-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="06021-112">Gibt alle Azure Site Recovery-Fabrics im Tresor zurück.</span><span class="sxs-lookup"><span data-stu-id="06021-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="06021-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="06021-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="06021-114">Geben Sie Azure Site Recovery Fabric mit dem Namen xxxx zurück.</span><span class="sxs-lookup"><span data-stu-id="06021-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="06021-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="06021-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="06021-116">Geben Sie Azure Site Recovery Fabric mit dem Anzeigenamen xxxx zurück.</span><span class="sxs-lookup"><span data-stu-id="06021-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="06021-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="06021-117">PARAMETERS</span></span>

### <span data-ttu-id="06021-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06021-118">-DefaultProfile</span></span>
<span data-ttu-id="06021-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06021-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="06021-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="06021-120">-FriendlyName</span></span>
<span data-ttu-id="06021-121">Suchen Sie nach dem ASR-Stoff anhand des Anzeigenamens des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="06021-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06021-122">-Name</span><span class="sxs-lookup"><span data-stu-id="06021-122">-Name</span></span>
<span data-ttu-id="06021-123">Suchen Sie nach dem ASR-Stoff nach dem Namen des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="06021-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="06021-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06021-124">CommonParameters</span></span>
<span data-ttu-id="06021-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06021-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06021-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06021-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06021-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06021-127">INPUTS</span></span>

### <span data-ttu-id="06021-128">Keine</span><span class="sxs-lookup"><span data-stu-id="06021-128">None</span></span>

## <span data-ttu-id="06021-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06021-129">OUTPUTS</span></span>

### <span data-ttu-id="06021-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="06021-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="06021-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="06021-131">NOTES</span></span>

## <span data-ttu-id="06021-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06021-132">RELATED LINKS</span></span>

[<span data-ttu-id="06021-133">Neu – AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="06021-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="06021-134">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="06021-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
