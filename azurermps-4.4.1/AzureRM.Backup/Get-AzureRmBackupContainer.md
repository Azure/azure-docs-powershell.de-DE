---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: c7bcddca0cfef631f7501dfb6c017f2c6ef7af25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662439"
---
# <span data-ttu-id="ea0de-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ea0de-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="ea0de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea0de-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0de-103">Ruft Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="ea0de-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea0de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea0de-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea0de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea0de-105">DESCRIPTION</span></span>
<span data-ttu-id="ea0de-106">Das Cmdlet " **Get-AzureRmBackupContainer** " ruft Azure-Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="ea0de-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="ea0de-107">Ein **AzureBackupContainer** kapselt Datenquellen, geschützte Elemente und Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="ea0de-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="ea0de-108">Eine **AzureBackupContainer** kann eine der folgenden Optionen sein:</span><span class="sxs-lookup"><span data-stu-id="ea0de-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="ea0de-109">Ein Windows Server-Computer</span><span class="sxs-lookup"><span data-stu-id="ea0de-109">A Windows Server computer</span></span>
- <span data-ttu-id="ea0de-110">Einen scdpm-Server (System Center Data Protection Manager)</span><span class="sxs-lookup"><span data-stu-id="ea0de-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="ea0de-111">Eine Azure Infrastructure as a Service (IaaS) Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="ea0de-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="ea0de-112">Bevor eine Datenquelle oder ein Element von der Sicherung gesichert werden kann, müssen Sie den Container, in dem Sie gespeichert ist, beim Azure-Sicherungsdienst registrieren.</span><span class="sxs-lookup"><span data-stu-id="ea0de-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="ea0de-113">Der Container muss authentifiziert werden, um Sicherungsdaten an den sicherungstresor zu senden.</span><span class="sxs-lookup"><span data-stu-id="ea0de-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="ea0de-114">Bei Windows Server-Computern und scdpm-Servern wird die Registrierung mit dem vollqualifizierten Domänennamen des Servers abgehalten.</span><span class="sxs-lookup"><span data-stu-id="ea0de-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="ea0de-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea0de-115">EXAMPLES</span></span>

### <span data-ttu-id="ea0de-116">Beispiel 1: Anzeigen aller für einen Tresor registrierten Server</span><span class="sxs-lookup"><span data-stu-id="ea0de-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="ea0de-117">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="ea0de-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ea0de-118">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="ea0de-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="ea0de-119">Der zweite Befehl ruft alle Container des Typs Windows aus dem Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="ea0de-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="ea0de-120">Beispiel 2: Abrufen eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="ea0de-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="ea0de-121">Dieser Befehl ruft den Container mit dem Namen DPMSERVER ab. CONTOSO.com.</span><span class="sxs-lookup"><span data-stu-id="ea0de-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="ea0de-122">Der Befehl gibt den Tresor in $Vault und den Typ des Containers an.</span><span class="sxs-lookup"><span data-stu-id="ea0de-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="ea0de-123">Beispiel 3: Anzeigen aller registrierten Azure Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="ea0de-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="ea0de-124">Dieser Befehl ruft die registrierten virtuellen Computer aus dem Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="ea0de-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="ea0de-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea0de-125">PARAMETERS</span></span>

### <span data-ttu-id="ea0de-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0de-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="ea0de-127">Gibt den Namen der Ressourcengruppe an, die dem Container zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ea0de-127">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="ea0de-128">Dieser Name ist derselbe Wert, den Sie für den *Service* Name-oder *ResourceGroupName* -Parameter des Register-AzureRmBackupContainer-Cmdlets angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="ea0de-128">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0de-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ea0de-129">-Name</span></span>
<span data-ttu-id="ea0de-130">Gibt den Namen des Containers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ea0de-130">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0de-131">-Status</span><span class="sxs-lookup"><span data-stu-id="ea0de-131">-Status</span></span>
<span data-ttu-id="ea0de-132">Gibt den aktuellen Status der Container an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ea0de-132">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="ea0de-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ea0de-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ea0de-134">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="ea0de-134">NotRegistered</span></span> 
- <span data-ttu-id="ea0de-135">Registriert</span><span class="sxs-lookup"><span data-stu-id="ea0de-135">Registered</span></span> 
- <span data-ttu-id="ea0de-136">Registrieren</span><span class="sxs-lookup"><span data-stu-id="ea0de-136">Registering</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0de-137">-Typ</span><span class="sxs-lookup"><span data-stu-id="ea0de-137">-Type</span></span>
<span data-ttu-id="ea0de-138">Gibt den Typ der Container an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ea0de-138">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0de-139">-Vault</span><span class="sxs-lookup"><span data-stu-id="ea0de-139">-Vault</span></span>
<span data-ttu-id="ea0de-140">Gibt einen sicherungstresor an, aus dem dieses Cmdlet Container erhält.</span><span class="sxs-lookup"><span data-stu-id="ea0de-140">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="ea0de-141">Verwenden Sie zum Abrufen eines **AzureRmBackupVault** das Get-AzureRmBackupVault-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea0de-141">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0de-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0de-142">-DefaultProfile</span></span>
<span data-ttu-id="ea0de-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea0de-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea0de-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0de-144">CommonParameters</span></span>
<span data-ttu-id="ea0de-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0de-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0de-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0de-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0de-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea0de-147">INPUTS</span></span>

### <span data-ttu-id="ea0de-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="ea0de-148">AzureBackupVault</span></span>

## <span data-ttu-id="ea0de-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea0de-149">OUTPUTS</span></span>

### <span data-ttu-id="ea0de-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ea0de-150">AzureBackupContainer</span></span>

## <span data-ttu-id="ea0de-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea0de-151">NOTES</span></span>
* <span data-ttu-id="ea0de-152">Keine</span><span class="sxs-lookup"><span data-stu-id="ea0de-152">None</span></span>

## <span data-ttu-id="ea0de-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea0de-153">RELATED LINKS</span></span>

[<span data-ttu-id="ea0de-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ea0de-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ea0de-155">Registrieren-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ea0de-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="ea0de-156">Registrierung aufheben-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ea0de-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


