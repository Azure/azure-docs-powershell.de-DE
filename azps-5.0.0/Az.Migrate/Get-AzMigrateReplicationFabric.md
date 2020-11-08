---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180275"
---
# <span data-ttu-id="b259a-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="b259a-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="b259a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b259a-102">SYNOPSIS</span></span>
<span data-ttu-id="b259a-103">Ruft die Details eines Azure Site Recovery-Fabrics ab.</span><span class="sxs-lookup"><span data-stu-id="b259a-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="b259a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b259a-104">SYNTAX</span></span>

### <span data-ttu-id="b259a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b259a-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b259a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b259a-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b259a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b259a-107">DESCRIPTION</span></span>
<span data-ttu-id="b259a-108">Ruft die Details eines Azure Site Recovery-Fabrics ab.</span><span class="sxs-lookup"><span data-stu-id="b259a-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="b259a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b259a-109">EXAMPLES</span></span>

### <span data-ttu-id="b259a-110">Beispiel 1: Abrufen aller Fabrics nach Ressourcengruppe und Vault-Name</span><span class="sxs-lookup"><span data-stu-id="b259a-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="b259a-111">Abrufen aller Fabrics in der Ressourcengruppe und im Tresor</span><span class="sxs-lookup"><span data-stu-id="b259a-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="b259a-112">Beispiel 2: Abrufen von Fabric nach Ressourcengruppe, Vault-Name und Fabric-Name</span><span class="sxs-lookup"><span data-stu-id="b259a-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="b259a-113">Abrufen eines bestimmten Gewebes</span><span class="sxs-lookup"><span data-stu-id="b259a-113">Get a specific fabric</span></span>

## <span data-ttu-id="b259a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b259a-114">PARAMETERS</span></span>

### <span data-ttu-id="b259a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b259a-115">-DefaultProfile</span></span>
<span data-ttu-id="b259a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b259a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b259a-117">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="b259a-117">-FabricName</span></span>
<span data-ttu-id="b259a-118">Name des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="b259a-118">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b259a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b259a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b259a-120">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b259a-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="b259a-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b259a-121">-ResourceName</span></span>
<span data-ttu-id="b259a-122">Der Name des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="b259a-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="b259a-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b259a-123">-SubscriptionId</span></span>
<span data-ttu-id="b259a-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b259a-124">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b259a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b259a-125">CommonParameters</span></span>
<span data-ttu-id="b259a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b259a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b259a-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b259a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b259a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b259a-128">INPUTS</span></span>

## <span data-ttu-id="b259a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b259a-129">OUTPUTS</span></span>

### <span data-ttu-id="b259a-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="b259a-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="b259a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b259a-131">NOTES</span></span>

<span data-ttu-id="b259a-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="b259a-132">ALIASES</span></span>

## <span data-ttu-id="b259a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b259a-133">RELATED LINKS</span></span>

