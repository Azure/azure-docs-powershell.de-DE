---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479369"
---
# <span data-ttu-id="c4bae-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="c4bae-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="c4bae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4bae-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bae-103">Ruft die Elemente unter einem Container in Backup ab.</span><span class="sxs-lookup"><span data-stu-id="c4bae-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4bae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4bae-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4bae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4bae-105">DESCRIPTION</span></span>
<span data-ttu-id="c4bae-106">Mit dem Cmdlet **Get-AzureRmBackupItem werden** die Elemente in einem Container in Azure Backup und der Schutzstatus der Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c4bae-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="c4bae-107">Aktivieren Sie Elemente für den Schutz mithilfe des Enable-AzureRmBackupProtection-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c4bae-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="c4bae-108">Ein Container, der für einen sicherungstresor registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="c4bae-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="c4bae-109">Für Azure Virtual Machines kann nur ein Element im Container für virtuelle Maschinen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c4bae-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="c4bae-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4bae-110">EXAMPLES</span></span>

### <span data-ttu-id="c4bae-111">Beispiel 1: Abrufen der Elemente in einem Container</span><span class="sxs-lookup"><span data-stu-id="c4bae-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="c4bae-112">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="c4bae-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="c4bae-113">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4bae-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="c4bae-114">Der zweite Befehl ruft mit dem Cmdlet **Get-AzureRmBackupContainer** einen Container mit dem angegebenen Namen im Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="c4bae-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="c4bae-115">Der Befehl speichert das Objekt in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4bae-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="c4bae-116">Der endgültige Befehl ruft das Sicherungselement im Container in $Container ab.</span><span class="sxs-lookup"><span data-stu-id="c4bae-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="c4bae-117">Beispiel 2: Anzeigen aller Eigenschaften für ein Element</span><span class="sxs-lookup"><span data-stu-id="c4bae-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="c4bae-118">Dieser Befehl ruft das Sicherungselement im Container in $Container ab und übergibt es dann an das Cmdlet Select-Object.</span><span class="sxs-lookup"><span data-stu-id="c4bae-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="c4bae-119">Dieses Cmdlet gibt alle Eigenschaften des sicherungselements zurück.</span><span class="sxs-lookup"><span data-stu-id="c4bae-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="c4bae-120">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="c4bae-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="c4bae-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4bae-121">PARAMETERS</span></span>

### <span data-ttu-id="c4bae-122">-Container</span><span class="sxs-lookup"><span data-stu-id="c4bae-122">-Container</span></span>
<span data-ttu-id="c4bae-123">Gibt ein Containerobjekt an, für das dieses Cmdlet Sicherungselemente erhält.</span><span class="sxs-lookup"><span data-stu-id="c4bae-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="c4bae-124">Verwenden Sie zum Abrufen eines **AzureRmBackupContainer** das Get-AzureRmBackupContainer-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4bae-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bae-125">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="c4bae-125">-ProtectionStatus</span></span>
<span data-ttu-id="c4bae-126">Gibt den allgemeinen Schutzstatus eines Elements im Container an.</span><span class="sxs-lookup"><span data-stu-id="c4bae-126">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="c4bae-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c4bae-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4bae-128">Geschützten</span><span class="sxs-lookup"><span data-stu-id="c4bae-128">Protected</span></span> 
- <span data-ttu-id="c4bae-129">Schutz</span><span class="sxs-lookup"><span data-stu-id="c4bae-129">Protecting</span></span>  
- <span data-ttu-id="c4bae-130">NotProtected</span><span class="sxs-lookup"><span data-stu-id="c4bae-130">NotProtected</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bae-131">-Status</span><span class="sxs-lookup"><span data-stu-id="c4bae-131">-Status</span></span>
<span data-ttu-id="c4bae-132">Gibt den Sicherungsstatus für ein Element an.</span><span class="sxs-lookup"><span data-stu-id="c4bae-132">Specifies the backup status for an item.</span></span>
<span data-ttu-id="c4bae-133">Die zulässigen Werte für diesen Parameter sind: IRPending, protected, ProtectionError und ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="c4bae-133">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="c4bae-134">Wenn der Wert des *ProtectionStatus* -Parameters geschützt ist, können Sie den *Status* -Parameterwert verwenden, um Elemente zu filtern.</span><span class="sxs-lookup"><span data-stu-id="c4bae-134">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bae-135">-Typ</span><span class="sxs-lookup"><span data-stu-id="c4bae-135">-Type</span></span>
<span data-ttu-id="c4bae-136">Gibt den Typ des Elements an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="c4bae-136">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="c4bae-137">Derzeit ist der einzige unterstützte Wert AzureVM.</span><span class="sxs-lookup"><span data-stu-id="c4bae-137">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bae-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bae-138">-DefaultProfile</span></span>
<span data-ttu-id="c4bae-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4bae-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4bae-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bae-140">CommonParameters</span></span>
<span data-ttu-id="c4bae-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bae-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bae-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4bae-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bae-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4bae-143">INPUTS</span></span>

### <span data-ttu-id="c4bae-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c4bae-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="c4bae-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4bae-145">OUTPUTS</span></span>

### <span data-ttu-id="c4bae-146">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="c4bae-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="c4bae-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4bae-147">NOTES</span></span>

## <span data-ttu-id="c4bae-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4bae-148">RELATED LINKS</span></span>

[<span data-ttu-id="c4bae-149">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="c4bae-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="c4bae-150">Deaktivieren-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c4bae-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="c4bae-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c4bae-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="c4bae-152">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="c4bae-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="c4bae-153">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c4bae-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="c4bae-154">Wiederherstellen – AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="c4bae-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


