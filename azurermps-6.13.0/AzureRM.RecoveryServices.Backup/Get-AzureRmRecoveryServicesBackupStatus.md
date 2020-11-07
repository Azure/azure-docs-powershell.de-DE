---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupStatus.md
ms.openlocfilehash: 00d7bb2c58abfa466b0c4843eb480b43b08b3d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664021"
---
# <span data-ttu-id="bc862-101">Get-AzureRmRecoveryServicesBackupStatus</span><span class="sxs-lookup"><span data-stu-id="bc862-101">Get-AzureRmRecoveryServicesBackupStatus</span></span>

## <span data-ttu-id="bc862-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bc862-102">SYNOPSIS</span></span>
<span data-ttu-id="bc862-103">Überprüft, ob Ihre Arm-Ressource gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="bc862-103">Checks whether your ARM resource is backed up or not.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc862-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc862-104">SYNTAX</span></span>

### <span data-ttu-id="bc862-105">Name (Standard)</span><span class="sxs-lookup"><span data-stu-id="bc862-105">Name (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc862-106">ID</span><span class="sxs-lookup"><span data-stu-id="bc862-106">Id</span></span>
```
Get-AzureRmRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc862-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc862-107">DESCRIPTION</span></span>
<span data-ttu-id="bc862-108">Der Befehl gibt NULL/Empty zurück, wenn die angegebene Ressource unter einem Vault für Wiederherstellungsdienste im Abonnement nicht geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bc862-108">The command returns null/empty if the specified resource is not protected under any Recovery Services vault in the subscription.</span></span> <span data-ttu-id="bc862-109">Wenn es geschützt ist, werden die entsprechenden Tresor-Details zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bc862-109">If it is protected, the relevant vault details will be returned.</span></span>

## <span data-ttu-id="bc862-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc862-110">EXAMPLES</span></span>

### <span data-ttu-id="bc862-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bc862-111">Example 1</span></span>
```
PS C:\> $status = Get-AzureRmRecoveryServicesBackupStatus -Name "myAzureVM" -ResourceGroupName "myAzureVMRG" -ResourceType "AzureVM"
PS C:\> If ($status.BackedUp -eq $false) {
$vault = Get-AzureRmRecoveryServicesVault -Name "testvault" -ResourceGroupName "vaultResourceGroup"
$defPolicy = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Vault $vault -WorkloadType "AzureVM"
Enable-AzureRmRecoveryServicesBackupProtection -Vault $vault -Policy $defpol -Name "myAzureVM" -ResourceGroupName "myAzureVMRG"
}
```

## <span data-ttu-id="bc862-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc862-112">PARAMETERS</span></span>

### <span data-ttu-id="bc862-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc862-113">-DefaultProfile</span></span>
<span data-ttu-id="bc862-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bc862-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc862-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bc862-115">-Name</span></span>
<span data-ttu-id="bc862-116">Der Name der Azure-Ressource, deren repräsentatives Element überprüft werden muss, wenn es bereits durch einen Vault für Wiederherstellungsdienste im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bc862-116">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc862-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc862-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc862-118">Der Name der Ressourcengruppe der Azure-Ressource, deren repräsentatives Element überprüft werden muss, wenn es bereits durch einige RecoveryServices-Tresor im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bc862-118">Name of the resource group of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc862-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="bc862-119">-ResourceId</span></span>
<span data-ttu-id="bc862-120">Die ID der Azure-Ressource, deren repräsentatives Element überprüft werden muss, wenn es bereits durch einige RecoveryServices-Tresor im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bc862-120">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc862-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="bc862-121">-Type</span></span>
<span data-ttu-id="bc862-122">Der Name der Azure-Ressource, deren repräsentatives Element überprüft werden muss, wenn es bereits durch einen Vault für Wiederherstellungsdienste im Abonnement geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="bc862-122">Name of the Azure Resource whose representative item needs to be checked if it is already protected by some Recovery Services Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc862-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc862-123">CommonParameters</span></span>
<span data-ttu-id="bc862-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc862-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc862-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc862-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc862-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bc862-126">INPUTS</span></span>

### <span data-ttu-id="bc862-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bc862-127">System.String</span></span>

## <span data-ttu-id="bc862-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bc862-128">OUTPUTS</span></span>

### <span data-ttu-id="bc862-129">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ResourceBackupStatus</span><span class="sxs-lookup"><span data-stu-id="bc862-129">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus</span></span>

## <span data-ttu-id="bc862-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="bc862-130">NOTES</span></span>

## <span data-ttu-id="bc862-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bc862-131">RELATED LINKS</span></span>
