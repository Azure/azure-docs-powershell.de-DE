---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006953"
---
# <span data-ttu-id="2213d-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="2213d-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="2213d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2213d-102">SYNOPSIS</span></span>


## <span data-ttu-id="2213d-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="2213d-103">SYNTAX</span></span>

### <span data-ttu-id="2213d-104">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="2213d-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2213d-105">Kontingentobject</span><span class="sxs-lookup"><span data-stu-id="2213d-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2213d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2213d-106">DESCRIPTION</span></span>


## <span data-ttu-id="2213d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2213d-107">EXAMPLES</span></span>

### <span data-ttu-id="2213d-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="2213d-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="2213d-109">Aktualisieren eines vorhandenen Speicherkontingents anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="2213d-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="2213d-110">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="2213d-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="2213d-111">Aktualisieren eines vorhandenen Speicherkontingents durch Piping</span><span class="sxs-lookup"><span data-stu-id="2213d-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="2213d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2213d-112">PARAMETERS</span></span>

### <span data-ttu-id="2213d-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="2213d-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2213d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2213d-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="2213d-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="2213d-115">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2213d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2213d-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2213d-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="2213d-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2213d-118">-Quotaobject</span><span class="sxs-lookup"><span data-stu-id="2213d-118">-QuotaObject</span></span>
<span data-ttu-id="2213d-119">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für kontingentobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2213d-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2213d-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2213d-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2213d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2213d-121">-Confirm</span></span>
<span data-ttu-id="2213d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2213d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2213d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2213d-123">-WhatIf</span></span>
<span data-ttu-id="2213d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2213d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2213d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2213d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2213d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2213d-126">CommonParameters</span></span>
<span data-ttu-id="2213d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2213d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2213d-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2213d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2213d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2213d-129">INPUTS</span></span>

### <span data-ttu-id="2213d-130">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="2213d-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="2213d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2213d-131">OUTPUTS</span></span>

### <span data-ttu-id="2213d-132">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="2213d-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="2213d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2213d-133">NOTES</span></span>

<span data-ttu-id="2213d-134">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2213d-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2213d-135">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2213d-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2213d-136">Quotaobject <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="2213d-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="2213d-137">`[CapacityInGb <Int32?>]`: Maximale Kapazität (GB).</span><span class="sxs-lookup"><span data-stu-id="2213d-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="2213d-138">`[NumberOfStorageAccounts <Int32?>]`: Gesamtzahl der Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="2213d-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="2213d-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2213d-139">RELATED LINKS</span></span>

