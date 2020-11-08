---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180267"
---
# <span data-ttu-id="4dc48-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4dc48-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="4dc48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4dc48-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc48-103">Ruft die Details des registrierten Wiederherstellungsdienste-Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="4dc48-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="4dc48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dc48-104">SYNTAX</span></span>

### <span data-ttu-id="4dc48-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4dc48-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4dc48-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4dc48-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4dc48-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dc48-107">DESCRIPTION</span></span>
<span data-ttu-id="4dc48-108">Ruft die Details des registrierten Wiederherstellungsdienste-Anbieters ab.</span><span class="sxs-lookup"><span data-stu-id="4dc48-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="4dc48-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dc48-109">EXAMPLES</span></span>

### <span data-ttu-id="4dc48-110">Beispiel 1: Abrufen aller Anbieter in Vault</span><span class="sxs-lookup"><span data-stu-id="4dc48-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="4dc48-111">Alle auflisten.</span><span class="sxs-lookup"><span data-stu-id="4dc48-111">List all.</span></span>

## <span data-ttu-id="4dc48-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dc48-112">PARAMETERS</span></span>

### <span data-ttu-id="4dc48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc48-113">-DefaultProfile</span></span>
<span data-ttu-id="4dc48-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4dc48-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc48-115">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="4dc48-115">-FabricName</span></span>
<span data-ttu-id="4dc48-116">Name des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="4dc48-116">Fabric name.</span></span>

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

### <span data-ttu-id="4dc48-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="4dc48-117">-ProviderName</span></span>
<span data-ttu-id="4dc48-118">Name des Dienstanbieters für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="4dc48-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="4dc48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc48-119">-ResourceGroupName</span></span>
<span data-ttu-id="4dc48-120">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4dc48-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="4dc48-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4dc48-121">-ResourceName</span></span>
<span data-ttu-id="4dc48-122">Der Name des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="4dc48-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="4dc48-123">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4dc48-123">-SubscriptionId</span></span>
<span data-ttu-id="4dc48-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4dc48-124">The subscription Id.</span></span>

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

### <span data-ttu-id="4dc48-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc48-125">CommonParameters</span></span>
<span data-ttu-id="4dc48-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dc48-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc48-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dc48-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc48-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4dc48-128">INPUTS</span></span>

## <span data-ttu-id="4dc48-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4dc48-129">OUTPUTS</span></span>

### <span data-ttu-id="4dc48-130">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4dc48-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="4dc48-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4dc48-131">NOTES</span></span>

<span data-ttu-id="4dc48-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="4dc48-132">ALIASES</span></span>

## <span data-ttu-id="4dc48-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4dc48-133">RELATED LINKS</span></span>

