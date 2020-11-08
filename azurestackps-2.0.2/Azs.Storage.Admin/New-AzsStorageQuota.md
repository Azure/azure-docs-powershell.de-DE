---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006803"
---
# <span data-ttu-id="548c5-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="548c5-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="548c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="548c5-102">SYNOPSIS</span></span>


## <span data-ttu-id="548c5-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="548c5-103">SYNTAX</span></span>

### <span data-ttu-id="548c5-104">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="548c5-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="548c5-105">Erstellen</span><span class="sxs-lookup"><span data-stu-id="548c5-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="548c5-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="548c5-106">DESCRIPTION</span></span>


## <span data-ttu-id="548c5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="548c5-107">EXAMPLES</span></span>

### <span data-ttu-id="548c5-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="548c5-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="548c5-109">Erstellen Sie ein neues Speicherkontingent mit angegebenen Werten.</span><span class="sxs-lookup"><span data-stu-id="548c5-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="548c5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="548c5-110">PARAMETERS</span></span>

### <span data-ttu-id="548c5-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="548c5-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="548c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548c5-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="548c5-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="548c5-113">-Location</span></span>


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

### <span data-ttu-id="548c5-114">-Name</span><span class="sxs-lookup"><span data-stu-id="548c5-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="548c5-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="548c5-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="548c5-116">-Quotaobject</span><span class="sxs-lookup"><span data-stu-id="548c5-116">-QuotaObject</span></span>
<span data-ttu-id="548c5-117">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für kontingentobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="548c5-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="548c5-118">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="548c5-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="548c5-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="548c5-119">-Confirm</span></span>
<span data-ttu-id="548c5-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="548c5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548c5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548c5-121">-WhatIf</span></span>
<span data-ttu-id="548c5-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="548c5-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548c5-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="548c5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548c5-124">CommonParameters</span></span>
<span data-ttu-id="548c5-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548c5-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="548c5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548c5-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="548c5-127">INPUTS</span></span>

### <span data-ttu-id="548c5-128">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="548c5-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="548c5-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="548c5-129">OUTPUTS</span></span>

### <span data-ttu-id="548c5-130">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="548c5-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="548c5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="548c5-131">NOTES</span></span>

<span data-ttu-id="548c5-132">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="548c5-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="548c5-133">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="548c5-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="548c5-134">Quotaobject <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="548c5-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="548c5-135">`[CapacityInGb <Int32?>]`: Maximale Kapazität (GB).</span><span class="sxs-lookup"><span data-stu-id="548c5-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="548c5-136">`[NumberOfStorageAccounts <Int32?>]`: Gesamtzahl der Speicherkonten.</span><span class="sxs-lookup"><span data-stu-id="548c5-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="548c5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="548c5-137">RELATED LINKS</span></span>

