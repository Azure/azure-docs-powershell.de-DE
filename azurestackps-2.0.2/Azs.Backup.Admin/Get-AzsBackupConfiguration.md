---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/get-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 3a9fedc637f8400b952d823a98dfe0abaa1d40d3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007247"
---
# <span data-ttu-id="f69ca-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69ca-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="f69ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f69ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f69ca-103">Gibt einen bestimmten Sicherungsspeicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="f69ca-103">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="f69ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f69ca-104">SYNTAX</span></span>

### <span data-ttu-id="f69ca-105">Abrufen (Standard)</span><span class="sxs-lookup"><span data-stu-id="f69ca-105">Get (Default)</span></span>
```
Get-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f69ca-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f69ca-106">GetViaIdentity</span></span>
```
Get-AzsBackupConfiguration -InputObject <IBackupAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f69ca-107">Liste</span><span class="sxs-lookup"><span data-stu-id="f69ca-107">List</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f69ca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f69ca-108">DESCRIPTION</span></span>
<span data-ttu-id="f69ca-109">Gibt einen bestimmten Sicherungsspeicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="f69ca-109">Returns a specific backup location based on name.</span></span>

## <span data-ttu-id="f69ca-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f69ca-110">EXAMPLES</span></span>

### <span data-ttu-id="f69ca-111">Beispiel 1: Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69ca-111">Example 1: Get-AzsBackupConfiguration</span></span>
```powershell
PS C:\> Get-AzsBackupConfiguration

```

<span data-ttu-id="f69ca-112">Erhalten Sie die Azure Stack-Sicherungskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f69ca-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="f69ca-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f69ca-113">PARAMETERS</span></span>

### <span data-ttu-id="f69ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69ca-114">-DefaultProfile</span></span>
<span data-ttu-id="f69ca-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f69ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f69ca-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f69ca-116">-InputObject</span></span>
<span data-ttu-id="f69ca-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f69ca-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f69ca-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="f69ca-118">-Location</span></span>
<span data-ttu-id="f69ca-119">Der Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="f69ca-119">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f69ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="f69ca-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f69ca-121">Name of the resource group.</span></span>

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

### <span data-ttu-id="f69ca-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="f69ca-122">-Skip</span></span>
<span data-ttu-id="f69ca-123">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="f69ca-123">OData skip parameter.</span></span>

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

### <span data-ttu-id="f69ca-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f69ca-124">-SubscriptionId</span></span>
<span data-ttu-id="f69ca-125">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f69ca-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f69ca-126">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f69ca-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f69ca-127">-Top</span><span class="sxs-lookup"><span data-stu-id="f69ca-127">-Top</span></span>
<span data-ttu-id="f69ca-128">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="f69ca-128">OData top parameter.</span></span>

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

### <span data-ttu-id="f69ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69ca-129">CommonParameters</span></span>
<span data-ttu-id="f69ca-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69ca-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f69ca-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69ca-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f69ca-132">INPUTS</span></span>

### <span data-ttu-id="f69ca-133">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f69ca-133">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="f69ca-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f69ca-134">OUTPUTS</span></span>

### <span data-ttu-id="f69ca-135">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="f69ca-135">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="f69ca-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="f69ca-136">NOTES</span></span>

<span data-ttu-id="f69ca-137">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f69ca-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f69ca-138">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f69ca-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f69ca-139">Inputobject <IBackupAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f69ca-139">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f69ca-140">`[Backup <String>]`: Name der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="f69ca-140">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="f69ca-141">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f69ca-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f69ca-142">`[Location <String>]`: Name des Sicherungsspeicherorts.</span><span class="sxs-lookup"><span data-stu-id="f69ca-142">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="f69ca-143">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f69ca-143">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f69ca-144">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f69ca-144">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f69ca-145">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f69ca-145">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f69ca-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f69ca-146">RELATED LINKS</span></span>

