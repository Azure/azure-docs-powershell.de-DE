---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005374"
---
# <span data-ttu-id="b2827-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b2827-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="b2827-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b2827-102">SYNOPSIS</span></span>


## <span data-ttu-id="b2827-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2827-103">SYNTAX</span></span>

### <span data-ttu-id="b2827-104">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="b2827-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b2827-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b2827-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b2827-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2827-106">DESCRIPTION</span></span>


## <span data-ttu-id="b2827-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2827-107">EXAMPLES</span></span>

### <span data-ttu-id="b2827-108">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="b2827-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="b2827-109">Entfernen eines Speicherkontingents nach Namen</span><span class="sxs-lookup"><span data-stu-id="b2827-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="b2827-110">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="b2827-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="b2827-111">Entfernen eines Speicherkontingents durch Piping</span><span class="sxs-lookup"><span data-stu-id="b2827-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="b2827-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2827-112">PARAMETERS</span></span>

### <span data-ttu-id="b2827-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2827-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="b2827-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2827-114">-InputObject</span></span>
<span data-ttu-id="b2827-115">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b2827-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b2827-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="b2827-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b2827-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2827-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b2827-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2827-118">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b2827-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b2827-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b2827-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b2827-120">-Confirm</span></span>
<span data-ttu-id="b2827-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b2827-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2827-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2827-122">-WhatIf</span></span>
<span data-ttu-id="b2827-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2827-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2827-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2827-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2827-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2827-125">CommonParameters</span></span>
<span data-ttu-id="b2827-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2827-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2827-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2827-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2827-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b2827-128">INPUTS</span></span>

### <span data-ttu-id="b2827-129">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b2827-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="b2827-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b2827-130">OUTPUTS</span></span>

### <span data-ttu-id="b2827-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2827-131">System.Boolean</span></span>



## <span data-ttu-id="b2827-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b2827-132">NOTES</span></span>

<span data-ttu-id="b2827-133">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b2827-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2827-134">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b2827-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b2827-135">Inputobject <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="b2827-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="b2827-136">`[AccountId <String>]`: Interne Speicherkonto-ID, die für den Mandanten nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="b2827-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="b2827-137">`[AsyncOperationId <String>]`: Async-Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="b2827-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="b2827-138">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="b2827-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2827-139">`[Location <String>]`: Ressourcen Standort.</span><span class="sxs-lookup"><span data-stu-id="b2827-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="b2827-140">`[QuotaName <String>]`: Der Name des Speicherkontingents.</span><span class="sxs-lookup"><span data-stu-id="b2827-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="b2827-141">`[ResourceGroup <String>]`: Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b2827-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="b2827-142">`[ServiceName <String>]`: Name des Speicher Diensts.</span><span class="sxs-lookup"><span data-stu-id="b2827-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="b2827-143">`[SubscriptionId <String>]`: Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b2827-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="b2827-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b2827-144">RELATED LINKS</span></span>

