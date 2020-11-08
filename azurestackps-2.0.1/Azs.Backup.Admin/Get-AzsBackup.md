---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackup
schema: 2.0.0
ms.openlocfilehash: 2c2d517da3be62ff407ca17577edefcf7322ad55
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005561"
---
# <span data-ttu-id="a6868-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="a6868-101">Get-AzsBackup</span></span>

## <span data-ttu-id="a6868-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6868-102">SYNOPSIS</span></span>
<span data-ttu-id="a6868-103">Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="a6868-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="a6868-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6868-104">SYNTAX</span></span>

### <span data-ttu-id="a6868-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6868-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a6868-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="a6868-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a6868-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a6868-107">GetViaIdentity</span></span>
```
Get-AzsBackup -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a6868-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6868-108">DESCRIPTION</span></span>
<span data-ttu-id="a6868-109">Gibt eine Sicherung von einem Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="a6868-109">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="a6868-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6868-110">EXAMPLES</span></span>

### <span data-ttu-id="a6868-111">Beispiel 1: Auflisten von Sicherungen</span><span class="sxs-lookup"><span data-stu-id="a6868-111">Example 1: List Backups</span></span>
```powershell
PS C:\> Get-AzsBackup

```

<span data-ttu-id="a6868-112">Abrufen von Informationen über alle Azure Stack-Sicherungen.</span><span class="sxs-lookup"><span data-stu-id="a6868-112">Get information sbout all Azure Stack backups.</span></span>

### <span data-ttu-id="a6868-113">Beispiel 2: Abrufen einer bestimmten Sicherung</span><span class="sxs-lookup"><span data-stu-id="a6868-113">Example 2: Get specific backup</span></span>
```powershell
PS C:\> Get-AzsBackup -Name 'backupName'

```

<span data-ttu-id="a6868-114">Rufen Sie Informationen für die angegebene Azure Stack-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="a6868-114">Get information for the the specified Azure Stack backup.</span></span>

## <span data-ttu-id="a6868-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6868-115">PARAMETERS</span></span>

### <span data-ttu-id="a6868-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6868-116">-DefaultProfile</span></span>
<span data-ttu-id="a6868-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6868-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6868-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6868-118">-InputObject</span></span>
<span data-ttu-id="a6868-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="a6868-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a6868-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="a6868-120">-Location</span></span>
<span data-ttu-id="a6868-121">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="a6868-121">Name of the backup location.</span></span>

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

### <span data-ttu-id="a6868-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a6868-122">-Name</span></span>
<span data-ttu-id="a6868-123">Der Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="a6868-123">Name of the backup.</span></span>

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

### <span data-ttu-id="a6868-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6868-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6868-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6868-125">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a6868-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="a6868-126">-Skip</span></span>
<span data-ttu-id="a6868-127">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="a6868-127">OData skip parameter.</span></span>

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

### <span data-ttu-id="a6868-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a6868-128">-SubscriptionId</span></span>
<span data-ttu-id="a6868-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a6868-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6868-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a6868-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a6868-131">-Top</span><span class="sxs-lookup"><span data-stu-id="a6868-131">-Top</span></span>
<span data-ttu-id="a6868-132">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="a6868-132">OData top parameter.</span></span>

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

### <span data-ttu-id="a6868-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6868-133">CommonParameters</span></span>
<span data-ttu-id="a6868-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6868-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6868-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6868-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6868-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6868-136">INPUTS</span></span>

### <span data-ttu-id="a6868-137">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a6868-137">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="a6868-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6868-138">OUTPUTS</span></span>

### <span data-ttu-id="a6868-139">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. ibackup</span><span class="sxs-lookup"><span data-stu-id="a6868-139">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackup</span></span>



## <span data-ttu-id="a6868-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6868-140">NOTES</span></span>

<span data-ttu-id="a6868-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a6868-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6868-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="a6868-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a6868-143">Inputobject <IBackupAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="a6868-143">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6868-144">`[Backup <String>]`: Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="a6868-144">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="a6868-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="a6868-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6868-146">`[Location <String>]`: Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="a6868-146">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="a6868-147">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a6868-147">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a6868-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a6868-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a6868-149">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="a6868-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a6868-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6868-150">RELATED LINKS</span></span>

