---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 3431650296c29f06131f946910d1cbc3dc6e6bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662528"
---
# <span data-ttu-id="40b1c-101">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="40b1c-101">Register-AzureRmBackupContainer</span></span>

## <span data-ttu-id="40b1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="40b1c-103">Registriert den Container mit einem Sicherungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="40b1c-103">Registers the container with a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40b1c-104">SYNTAX</span></span>

### <span data-ttu-id="40b1c-105">V1VM</span><span class="sxs-lookup"><span data-stu-id="40b1c-105">V1VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b1c-106">V2VM</span><span class="sxs-lookup"><span data-stu-id="40b1c-106">V2VM</span></span>
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40b1c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40b1c-107">DESCRIPTION</span></span>
<span data-ttu-id="40b1c-108">Mit dem Cmdlet " **Register-AzureRmBackupContainer** " wird der Container mit einem Azure Backup Vault registriert.</span><span class="sxs-lookup"><span data-stu-id="40b1c-108">The **Register-AzureRmBackupContainer** cmdlet registers the container with an Azure Backup vault.</span></span>
<span data-ttu-id="40b1c-109">Wenn Sie die Sicherung mithilfe der Azure-Sicherung konfigurieren möchten, registrieren Sie zuerst Ihren Server oder virtuellen Computer mit einem Sicherungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="40b1c-109">To configure backup by using Azure Backup, first register your server or virtual machine with a Backup vault.</span></span>
<span data-ttu-id="40b1c-110">Mit diesem Cmdlet wird eine Infrastruktur als IaaS-virtueller Computer mit dem angegebenen Tresor registriert.</span><span class="sxs-lookup"><span data-stu-id="40b1c-110">This cmdlet registers an infrastructure as a service (IaaS) virtual machine with the specified vault.</span></span>
<span data-ttu-id="40b1c-111">Der Vorgang registrieren ordnet den Azure Virtual Machine dem Sicherungsspeicher zu und verfolgt den virtuellen Computer über den Lebenszyklus der Sicherung.</span><span class="sxs-lookup"><span data-stu-id="40b1c-111">The register operation associates the Azure virtual machine with the backup vault and tracks the virtual machine through the backup life cycle.</span></span>

## <span data-ttu-id="40b1c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40b1c-112">EXAMPLES</span></span>

### <span data-ttu-id="40b1c-113">Beispiel 1: Registrieren eines virtuellen Computers in einem Sicherungsspeicher</span><span class="sxs-lookup"><span data-stu-id="40b1c-113">Example 1: Register a virtual machine to a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

<span data-ttu-id="40b1c-114">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="40b1c-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="40b1c-115">Der Befehl speichert den Tresor in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="40b1c-115">The command stores the vault in the $Vault variable.</span></span>
<span data-ttu-id="40b1c-116">Der zweite Befehl registriert den virtuellen Computer mit dem Namen Contoso03Vm mit dem Tresor in $Vault.</span><span class="sxs-lookup"><span data-stu-id="40b1c-116">The second command registers the virtual machine named Contoso03Vm with the vault in $Vault.</span></span>
<span data-ttu-id="40b1c-117">Dieser virtuelle Computer gehört zum Dienst mit dem Namen ContosoService27.</span><span class="sxs-lookup"><span data-stu-id="40b1c-117">That virtual machine belongs to the service named ContosoService27.</span></span>

## <span data-ttu-id="40b1c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="40b1c-118">PARAMETERS</span></span>

### <span data-ttu-id="40b1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b1c-119">-DefaultProfile</span></span>
<span data-ttu-id="40b1c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="40b1c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40b1c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="40b1c-121">-Name</span></span>
<span data-ttu-id="40b1c-122">Gibt den Namen des virtuellen Computers an, der von diesem Cmdlet registriert wird.</span><span class="sxs-lookup"><span data-stu-id="40b1c-122">Specifies the name of the virtual machine that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="40b1c-124">Gibt den Namen der Ressourcengruppe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="40b1c-124">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b1c-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="40b1c-125">-ServiceName</span></span>
<span data-ttu-id="40b1c-126">Gibt den Dienstnamen des virtuellen Computers an, den dieses Cmdlet registriert.</span><span class="sxs-lookup"><span data-stu-id="40b1c-126">Specifies the service name of the virtual machine that this cmdlet registers.</span></span>
<span data-ttu-id="40b1c-127">In der Regel weist ein Cloud-Dienstname ein Suffix. cloudapp.net auf.</span><span class="sxs-lookup"><span data-stu-id="40b1c-127">Typically, a cloud service name has a suffix .cloudapp.net.</span></span>
<span data-ttu-id="40b1c-128">Schließen Sie das Suffix nicht ein, wenn Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="40b1c-128">Do not include the suffix when you specify this parameter.</span></span>
<span data-ttu-id="40b1c-129">Verwenden Sie das Get-AzureRMVM-Cmdlet, um Informationen zu einem virtuellen Computer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="40b1c-129">To obtain information about a virtual machine, use the Get-AzureRMVM cmdlet.</span></span>
<span data-ttu-id="40b1c-130">Der Dienstname ist die **deploymentname** -Eigenschaft des Virtual Machine-Objekts.</span><span class="sxs-lookup"><span data-stu-id="40b1c-130">The service name is the **DeploymentName** property of the virtual machine object.</span></span>

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b1c-131">-Vault</span><span class="sxs-lookup"><span data-stu-id="40b1c-131">-Vault</span></span>
<span data-ttu-id="40b1c-132">Gibt den sicherungstresor an, zu dem dieses Cmdlet den virtuellen Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="40b1c-132">Specifies the Backup vault to which this cmdlet registers virtual machine.</span></span>
<span data-ttu-id="40b1c-133">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="40b1c-133">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="40b1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b1c-134">CommonParameters</span></span>
<span data-ttu-id="40b1c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b1c-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b1c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b1c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40b1c-137">INPUTS</span></span>

### <span data-ttu-id="40b1c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="40b1c-138">System.String</span></span>

### <span data-ttu-id="40b1c-139">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="40b1c-139">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="40b1c-140">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="40b1c-140">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="40b1c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40b1c-141">OUTPUTS</span></span>

### <span data-ttu-id="40b1c-142">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="40b1c-142">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="40b1c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="40b1c-143">NOTES</span></span>

## <span data-ttu-id="40b1c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40b1c-144">RELATED LINKS</span></span>

[<span data-ttu-id="40b1c-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="40b1c-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


