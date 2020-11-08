---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005533"
---
# <span data-ttu-id="0435a-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0435a-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="0435a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0435a-102">SYNOPSIS</span></span>
<span data-ttu-id="0435a-103">Gibt das angeforderte Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="0435a-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="0435a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0435a-104">SYNTAX</span></span>

### <span data-ttu-id="0435a-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0435a-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0435a-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0435a-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0435a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0435a-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0435a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0435a-108">DESCRIPTION</span></span>
<span data-ttu-id="0435a-109">Gibt das angeforderte Speicherkonto zurück.</span><span class="sxs-lookup"><span data-stu-id="0435a-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="0435a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0435a-110">EXAMPLES</span></span>

### <span data-ttu-id="0435a-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="0435a-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="0435a-112">Abrufen einer Liste von Speicherkonten (Zusammenfassung).</span><span class="sxs-lookup"><span data-stu-id="0435a-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="0435a-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="0435a-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="0435a-114">Rufen Sie eine Liste des speicherkontos mit Details ab, und Drucken Sie den Status.</span><span class="sxs-lookup"><span data-stu-id="0435a-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="0435a-115">Beispiel 3:</span><span class="sxs-lookup"><span data-stu-id="0435a-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="0435a-116">Abrufen von Details des angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="0435a-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="0435a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="0435a-117">PARAMETERS</span></span>

### <span data-ttu-id="0435a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0435a-118">-DefaultProfile</span></span>
<span data-ttu-id="0435a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0435a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0435a-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="0435a-120">-Filter</span></span>
<span data-ttu-id="0435a-121">Filter Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0435a-121">Filter string</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0435a-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0435a-122">-InputObject</span></span>
<span data-ttu-id="0435a-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0435a-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0435a-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="0435a-124">-Location</span></span>
<span data-ttu-id="0435a-125">Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="0435a-125">Resource location.</span></span>

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

### <span data-ttu-id="0435a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0435a-126">-Name</span></span>
<span data-ttu-id="0435a-127">Interne Speicherkonto-ID, die für den Mandanten nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="0435a-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0435a-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0435a-128">-SubscriptionId</span></span>
<span data-ttu-id="0435a-129">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0435a-129">Subscription Id.</span></span>

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

### <span data-ttu-id="0435a-130">– Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0435a-130">-Summary</span></span>
<span data-ttu-id="0435a-131">Wechseln Sie dazu, ob Zusammenfassungs-oder Detailinformationen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0435a-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0435a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0435a-132">CommonParameters</span></span>
<span data-ttu-id="0435a-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0435a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0435a-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0435a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0435a-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0435a-135">INPUTS</span></span>

### <span data-ttu-id="0435a-136">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0435a-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="0435a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0435a-137">OUTPUTS</span></span>

### <span data-ttu-id="0435a-138">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0435a-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="0435a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0435a-139">NOTES</span></span>

<span data-ttu-id="0435a-140">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0435a-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0435a-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0435a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0435a-142">Inputobject <IStorageAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="0435a-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0435a-143">`[AccountId <String>]`: Interne Speicherkonto-ID, die für den Mandanten nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="0435a-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="0435a-144">`[AsyncOperationId <String>]`: Async-Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="0435a-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="0435a-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="0435a-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0435a-146">`[Location <String>]`: Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="0435a-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="0435a-147">`[QuotaName <String>]`: Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="0435a-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="0435a-148">`[ResourceGroup <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0435a-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="0435a-149">`[ServiceName <String>]`: Name des Speicher Diensts.</span><span class="sxs-lookup"><span data-stu-id="0435a-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="0435a-150">`[SubscriptionId <String>]`: Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0435a-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="0435a-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0435a-151">RELATED LINKS</span></span>

