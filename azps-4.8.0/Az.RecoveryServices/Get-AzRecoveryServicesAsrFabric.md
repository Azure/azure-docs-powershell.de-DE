---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: c3bd5ecf7e3561be5f9e6b8d990c40281135982c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174227"
---
# <span data-ttu-id="57179-101">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="57179-101">Get-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="57179-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57179-102">SYNOPSIS</span></span>
<span data-ttu-id="57179-103">Abrufen der Details eines Azure Site Recovery-Fabrics</span><span class="sxs-lookup"><span data-stu-id="57179-103">Get the details of an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="57179-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57179-104">SYNTAX</span></span>

### <span data-ttu-id="57179-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="57179-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57179-106">ByName</span><span class="sxs-lookup"><span data-stu-id="57179-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57179-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="57179-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57179-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57179-108">DESCRIPTION</span></span>
<span data-ttu-id="57179-109">Das Cmdlet " **Get-AzRecoveryServicesAsrFabric** " Ruft die Eigenschaften eines angegebenen Azure Site Recovery-Fabrics oder aller Azure Site Recovery-Fabrics in einem Recovery Service Vault ab.</span><span class="sxs-lookup"><span data-stu-id="57179-109">The **Get-AzRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="57179-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57179-110">EXAMPLES</span></span>

### <span data-ttu-id="57179-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="57179-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzRecoveryServicesAsrFabric
```

<span data-ttu-id="57179-112">Gibt alle Azure Site Recovery-Fabrics im Tresor zurück.</span><span class="sxs-lookup"><span data-stu-id="57179-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="57179-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="57179-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="57179-114">Geben Sie Azure Site Recovery Fabric mit dem Namen xxxx zurück.</span><span class="sxs-lookup"><span data-stu-id="57179-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="57179-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="57179-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="57179-116">Geben Sie Azure Site Recovery Fabric mit dem Anzeigenamen xxxx zurück.</span><span class="sxs-lookup"><span data-stu-id="57179-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="57179-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="57179-117">PARAMETERS</span></span>

### <span data-ttu-id="57179-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57179-118">-DefaultProfile</span></span>
<span data-ttu-id="57179-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57179-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57179-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="57179-120">-FriendlyName</span></span>
<span data-ttu-id="57179-121">Suchen Sie nach dem ASR-Stoff anhand des Anzeigenamens des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="57179-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="57179-122">-Name</span><span class="sxs-lookup"><span data-stu-id="57179-122">-Name</span></span>
<span data-ttu-id="57179-123">Suchen Sie nach dem ASR-Stoff nach dem Namen des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="57179-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="57179-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57179-124">CommonParameters</span></span>
<span data-ttu-id="57179-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57179-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57179-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57179-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57179-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57179-127">INPUTS</span></span>

### <span data-ttu-id="57179-128">Keine</span><span class="sxs-lookup"><span data-stu-id="57179-128">None</span></span>

## <span data-ttu-id="57179-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57179-129">OUTPUTS</span></span>

### <span data-ttu-id="57179-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="57179-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="57179-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="57179-131">NOTES</span></span>

## <span data-ttu-id="57179-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57179-132">RELATED LINKS</span></span>

[<span data-ttu-id="57179-133">Neu – AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="57179-133">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="57179-134">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="57179-134">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
