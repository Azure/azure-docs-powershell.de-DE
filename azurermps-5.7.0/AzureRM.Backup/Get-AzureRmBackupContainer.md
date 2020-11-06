---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: abc4bce43c5be267e736cb93e03806cdd802fcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478774"
---
# <span data-ttu-id="55fe8-101">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="55fe8-101">Get-AzureRmBackupContainer</span></span>

## <span data-ttu-id="55fe8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="55fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="55fe8-103">Ruft Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="55fe8-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55fe8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="55fe8-104">SYNTAX</span></span>

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55fe8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55fe8-105">DESCRIPTION</span></span>
<span data-ttu-id="55fe8-106">Das Cmdlet " **Get-AzureRmBackupContainer** " ruft Azure-Sicherungs Container ab.</span><span class="sxs-lookup"><span data-stu-id="55fe8-106">The **Get-AzureRmBackupContainer** cmdlet gets Azure Backup containers.</span></span>

<span data-ttu-id="55fe8-107">Ein **AzureBackupContainer** kapselt Datenquellen, geschützte Elemente und Wiederherstellungspunkte.</span><span class="sxs-lookup"><span data-stu-id="55fe8-107">An **AzureBackupContainer** encapsulates data sources, protected items, and recovery points.</span></span>
<span data-ttu-id="55fe8-108">Eine **AzureBackupContainer** kann eine der folgenden Optionen sein:</span><span class="sxs-lookup"><span data-stu-id="55fe8-108">An **AzureBackupContainer** can be one of the following:</span></span> 

- <span data-ttu-id="55fe8-109">Ein Windows Server-Computer</span><span class="sxs-lookup"><span data-stu-id="55fe8-109">A Windows Server computer</span></span>
- <span data-ttu-id="55fe8-110">Einen scdpm-Server (System Center Data Protection Manager)</span><span class="sxs-lookup"><span data-stu-id="55fe8-110">A System Center Data Protection Manager (SCDPM) server</span></span> 
- <span data-ttu-id="55fe8-111">Eine Azure Infrastructure as a Service (IaaS) Virtual Machine</span><span class="sxs-lookup"><span data-stu-id="55fe8-111">An Azure infrastructure as a service (IaaS) virtual machine</span></span>

<span data-ttu-id="55fe8-112">Bevor eine Datenquelle oder ein Element von der Sicherung gesichert werden kann, müssen Sie den Container, in dem Sie gespeichert ist, beim Azure-Sicherungsdienst registrieren.</span><span class="sxs-lookup"><span data-stu-id="55fe8-112">Before Backup can back up a data source or item, you must register the container that holds it with the Azure Backup service.</span></span>
<span data-ttu-id="55fe8-113">Der Container muss authentifiziert werden, um Sicherungsdaten an den sicherungstresor zu senden.</span><span class="sxs-lookup"><span data-stu-id="55fe8-113">The container must be authenticated to send backup data to the Backup vault.</span></span>
<span data-ttu-id="55fe8-114">Bei Windows Server-Computern und scdpm-Servern wird die Registrierung mit dem vollqualifizierten Domänennamen des Servers abgehalten.</span><span class="sxs-lookup"><span data-stu-id="55fe8-114">For Windows Server computers and SCDPM servers, the registration is held with the fully qualified domain name of the server.</span></span>

## <span data-ttu-id="55fe8-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="55fe8-115">EXAMPLES</span></span>

### <span data-ttu-id="55fe8-116">Beispiel 1: Anzeigen aller für einen Tresor registrierten Server</span><span class="sxs-lookup"><span data-stu-id="55fe8-116">Example 1: View all servers registered to a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

<span data-ttu-id="55fe8-117">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="55fe8-117">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="55fe8-118">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="55fe8-118">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="55fe8-119">Der zweite Befehl ruft alle Container des Typs Windows aus dem Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="55fe8-119">The second command gets all containers of type Windows from the vault in $Vault.</span></span>

### <span data-ttu-id="55fe8-120">Beispiel 2: Abrufen eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="55fe8-120">Example 2: Get a specific container</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

<span data-ttu-id="55fe8-121">Dieser Befehl ruft den Container mit dem Namen DPMSERVER ab. CONTOSO.com.</span><span class="sxs-lookup"><span data-stu-id="55fe8-121">This command gets the container named DPMSERVER.CONTOSO.COM.</span></span>
<span data-ttu-id="55fe8-122">Der Befehl gibt den Tresor in $Vault und den Typ des Containers an.</span><span class="sxs-lookup"><span data-stu-id="55fe8-122">The command specifies the vault in $Vault and the type of container.</span></span>

### <span data-ttu-id="55fe8-123">Beispiel 3: Anzeigen aller registrierten Azure Virtual Machines</span><span class="sxs-lookup"><span data-stu-id="55fe8-123">Example 3: View all registered Azure virtual machines</span></span>
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

<span data-ttu-id="55fe8-124">Dieser Befehl ruft die registrierten virtuellen Computer aus dem Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="55fe8-124">This command gets the registered virtual machines from the vault in $Vault.</span></span>

## <span data-ttu-id="55fe8-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="55fe8-125">PARAMETERS</span></span>

### <span data-ttu-id="55fe8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fe8-126">-DefaultProfile</span></span>
<span data-ttu-id="55fe8-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="55fe8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fe8-128">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55fe8-128">-ManagedResourceGroupName</span></span>
<span data-ttu-id="55fe8-129">Gibt den Namen der Ressourcengruppe an, die dem Container zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="55fe8-129">Specifies the name of the resource group associated with the container.</span></span>
<span data-ttu-id="55fe8-130">Dieser Name ist derselbe Wert, den Sie für den *Service* Name-oder *ResourceGroupName* -Parameter des Register-AzureRmBackupContainer-Cmdlets angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="55fe8-130">This name is the same value that you specified for the *ServiceName* or *ResourceGroupName* parameter of the Register-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fe8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="55fe8-131">-Name</span></span>
<span data-ttu-id="55fe8-132">Gibt den Namen des Containers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="55fe8-132">Specifies the name of the container that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fe8-133">-Status</span><span class="sxs-lookup"><span data-stu-id="55fe8-133">-Status</span></span>
<span data-ttu-id="55fe8-134">Gibt den aktuellen Status der Container an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="55fe8-134">Specifies the current status of the containers that this cmdlet gets.</span></span>
<span data-ttu-id="55fe8-135">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="55fe8-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="55fe8-136">NotRegistered</span><span class="sxs-lookup"><span data-stu-id="55fe8-136">NotRegistered</span></span> 
- <span data-ttu-id="55fe8-137">Registriert</span><span class="sxs-lookup"><span data-stu-id="55fe8-137">Registered</span></span> 
- <span data-ttu-id="55fe8-138">Registrieren</span><span class="sxs-lookup"><span data-stu-id="55fe8-138">Registering</span></span>

```yaml
Type: AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fe8-139">-Typ</span><span class="sxs-lookup"><span data-stu-id="55fe8-139">-Type</span></span>
<span data-ttu-id="55fe8-140">Gibt den Typ der Container an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="55fe8-140">Specifies the type of containers that this cmdlet gets.</span></span>

```yaml
Type: AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fe8-141">-Vault</span><span class="sxs-lookup"><span data-stu-id="55fe8-141">-Vault</span></span>
<span data-ttu-id="55fe8-142">Gibt einen sicherungstresor an, aus dem dieses Cmdlet Container erhält.</span><span class="sxs-lookup"><span data-stu-id="55fe8-142">Specifies a Backup vault from which this cmdlet gets containers.</span></span>
<span data-ttu-id="55fe8-143">Verwenden Sie zum Abrufen eines **AzureRmBackupVault** das Get-AzureRmBackupVault-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55fe8-143">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55fe8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fe8-144">CommonParameters</span></span>
<span data-ttu-id="55fe8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55fe8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fe8-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55fe8-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fe8-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="55fe8-147">INPUTS</span></span>

### <span data-ttu-id="55fe8-148">AzureBackupVault</span><span class="sxs-lookup"><span data-stu-id="55fe8-148">AzureBackupVault</span></span>

## <span data-ttu-id="55fe8-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="55fe8-149">OUTPUTS</span></span>

### <span data-ttu-id="55fe8-150">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="55fe8-150">AzureBackupContainer</span></span>

## <span data-ttu-id="55fe8-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="55fe8-151">NOTES</span></span>
* <span data-ttu-id="55fe8-152">Keine</span><span class="sxs-lookup"><span data-stu-id="55fe8-152">None</span></span>

## <span data-ttu-id="55fe8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="55fe8-153">RELATED LINKS</span></span>

[<span data-ttu-id="55fe8-154">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="55fe8-154">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="55fe8-155">Registrieren-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="55fe8-155">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)

[<span data-ttu-id="55fe8-156">Registrierung aufheben-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="55fe8-156">Unregister-AzureRmBackupContainer</span></span>](./Unregister-AzureRmBackupContainer.md)


