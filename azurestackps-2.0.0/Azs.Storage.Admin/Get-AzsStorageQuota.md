---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "94005291"
---
# <span data-ttu-id="f1310-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f1310-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="f1310-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1310-102">SYNOPSIS</span></span>


## <span data-ttu-id="f1310-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1310-103">SYNTAX</span></span>

### <span data-ttu-id="f1310-104">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f1310-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1310-105">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f1310-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f1310-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f1310-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f1310-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1310-107">DESCRIPTION</span></span>


## <span data-ttu-id="f1310-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1310-108">EXAMPLES</span></span>

### <span data-ttu-id="f1310-109">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="f1310-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="f1310-110">Rufen Sie die Liste der Speicherkontingente ab.</span><span class="sxs-lookup"><span data-stu-id="f1310-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="f1310-111">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="f1310-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="f1310-112">Abrufen von Details des angegebenen Speicherkontingents anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="f1310-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="f1310-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1310-113">PARAMETERS</span></span>

### <span data-ttu-id="f1310-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1310-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="f1310-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1310-115">-InputObject</span></span>
<span data-ttu-id="f1310-116">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f1310-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="f1310-117">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f1310-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f1310-119">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f1310-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1310-120">CommonParameters</span></span>
<span data-ttu-id="f1310-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1310-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1310-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1310-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1310-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1310-123">INPUTS</span></span>

### <span data-ttu-id="f1310-124">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f1310-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="f1310-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1310-125">OUTPUTS</span></span>

### <span data-ttu-id="f1310-126">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="f1310-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="f1310-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1310-127">NOTES</span></span>

<span data-ttu-id="f1310-128">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f1310-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f1310-129">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f1310-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f1310-130">Inputobject <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="f1310-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="f1310-131">`[AccountId <String>]`: Interne Speicherkonto-ID, die für den Mandanten nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="f1310-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="f1310-132">`[AsyncOperationId <String>]`: Async-Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="f1310-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="f1310-133">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f1310-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f1310-134">`[Location <String>]`: Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="f1310-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="f1310-135">`[QuotaName <String>]`: Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="f1310-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="f1310-136">`[ResourceGroup <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f1310-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="f1310-137">`[ServiceName <String>]`: Name des Speicher Diensts.</span><span class="sxs-lookup"><span data-stu-id="f1310-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="f1310-138">`[SubscriptionId <String>]`: Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="f1310-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="f1310-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1310-139">RELATED LINKS</span></span>

