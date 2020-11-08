---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 8bc2286cf6df736ee54390447e83f0337c031001
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004914"
---
# <span data-ttu-id="a3816-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a3816-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="a3816-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3816-102">SYNOPSIS</span></span>
<span data-ttu-id="a3816-103">Dieser Befehl löst die Erkennung ungeschützter Elemente des angegebenen Arbeits Auslastungs Typs im angegebenen Container aus.</span><span class="sxs-lookup"><span data-stu-id="a3816-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="a3816-104">Wenn die DB-Anwendung nicht automatisch geschützt ist, verwenden Sie diesen Befehl, um neue DBS zu erkennen, wenn Sie hinzugefügt werden, und gehen Sie zum Schutz.</span><span class="sxs-lookup"><span data-stu-id="a3816-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="a3816-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3816-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3816-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3816-106">DESCRIPTION</span></span>
<span data-ttu-id="a3816-107">das Cmdlet fragt nach bestimmten Arbeitslasten innerhalb eines Containers.</span><span class="sxs-lookup"><span data-stu-id="a3816-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="a3816-108">Dadurch wird ein Vorgang ausgelöst, der geschützte Elemente erstellt.</span><span class="sxs-lookup"><span data-stu-id="a3816-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="a3816-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3816-109">EXAMPLES</span></span>

### <span data-ttu-id="a3816-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3816-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container -WorkloadType "MSSQL"
```

<span data-ttu-id="a3816-111">Das Cmdlet führt einen Ermittlungsvorgang für neue geschützte Elemente aus.</span><span class="sxs-lookup"><span data-stu-id="a3816-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="a3816-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3816-112">PARAMETERS</span></span>

### <span data-ttu-id="a3816-113">-Container</span><span class="sxs-lookup"><span data-stu-id="a3816-113">-Container</span></span>
<span data-ttu-id="a3816-114">Container, in dem sich das Element befindet</span><span class="sxs-lookup"><span data-stu-id="a3816-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3816-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3816-115">-DefaultProfile</span></span>
<span data-ttu-id="a3816-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3816-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3816-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3816-117">-PassThru</span></span>
<span data-ttu-id="a3816-118">Geben Sie den zu löschenden Container zurück.</span><span class="sxs-lookup"><span data-stu-id="a3816-118">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="a3816-119">-Tresor</span><span class="sxs-lookup"><span data-stu-id="a3816-119">-VaultId</span></span>
<span data-ttu-id="a3816-120">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="a3816-120">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3816-121">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="a3816-121">-WorkloadType</span></span>
<span data-ttu-id="a3816-122">Arbeits Auslastungs der Ressource (Beispiel: AzureVM, Windows Server, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="a3816-122">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3816-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3816-123">-Confirm</span></span>
<span data-ttu-id="a3816-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3816-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3816-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3816-125">-WhatIf</span></span>
<span data-ttu-id="a3816-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3816-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3816-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3816-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3816-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3816-128">CommonParameters</span></span>
<span data-ttu-id="a3816-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3816-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3816-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3816-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3816-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3816-131">INPUTS</span></span>

### <span data-ttu-id="a3816-132">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="a3816-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="a3816-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a3816-133">System.String</span></span>

## <span data-ttu-id="a3816-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3816-134">OUTPUTS</span></span>

### <span data-ttu-id="a3816-135">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="a3816-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="a3816-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3816-136">NOTES</span></span>

## <span data-ttu-id="a3816-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3816-137">RELATED LINKS</span></span>
