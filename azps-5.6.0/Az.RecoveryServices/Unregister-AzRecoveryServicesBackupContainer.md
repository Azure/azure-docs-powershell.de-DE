---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 94f46616d9d1bbf15159ed086b227c47d042799b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941443"
---
# <span data-ttu-id="6cf6e-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6cf6e-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="6cf6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf6e-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf6e-103">Registriert einen Windows Server oder einen anderen Container aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="6cf6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cf6e-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cf6e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cf6e-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf6e-106">Das **Cmdlet "Unregister-AzRecoveryServicesBackupContainer"** entfernt die Registrierung eines Windows Server- oder anderen Sicherungscontainers aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="6cf6e-107">Mit diesem Cmdlet werden Verweise auf einen Container aus dem Tresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="6cf6e-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="6cf6e-109">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6cf6e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6cf6e-110">EXAMPLES</span></span>

### <span data-ttu-id="6cf6e-111">Beispiel 1: Aufheben der Registrierung eines Windows Servers aus dem Tresor</span><span class="sxs-lookup"><span data-stu-id="6cf6e-111">Example 1: Unregister a Windows Server from the vault</span></span>
```powershell
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="6cf6e-112">Der erste Befehl ruft den Windows-Container server01.contoso.com ab, der im Tresor registriert ist, und speichert ihn dann in der $Cont Variablen.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="6cf6e-113">Mit dem zweiten Befehl wird die Registrierung des angegebenen Windows Server aus dem Azure Backup-Tresor aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="6cf6e-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6cf6e-114">Example 2</span></span>

<span data-ttu-id="6cf6e-115">Registriert einen Windows Server oder einen anderen Container aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-115">Unregisters a Windows Server or other container from the vault.</span></span> <span data-ttu-id="6cf6e-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="6cf6e-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupContainer -Container $Cont -VaultId $vault.ID
```

## <span data-ttu-id="6cf6e-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6cf6e-117">PARAMETERS</span></span>

### <span data-ttu-id="6cf6e-118">-Container</span><span class="sxs-lookup"><span data-stu-id="6cf6e-118">-Container</span></span>
<span data-ttu-id="6cf6e-119">Gibt ein Sicherungscontainerobjekt an, das die Registrierung aufheben soll.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-119">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="6cf6e-120">Um ein **BackupContainer-Objekt** zu erhalten, verwenden Sie das Get-AzRecoveryServicesBackupContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-120">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf6e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf6e-121">-DefaultProfile</span></span>
<span data-ttu-id="6cf6e-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cf6e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6cf6e-123">-PassThru</span></span>
<span data-ttu-id="6cf6e-124">Geben Sie den zu löschende Container zurück.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-124">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="6cf6e-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6cf6e-125">-VaultId</span></span>
<span data-ttu-id="6cf6e-126">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6cf6e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6cf6e-127">-Confirm</span></span>
<span data-ttu-id="6cf6e-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cf6e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cf6e-129">-WhatIf</span></span>
<span data-ttu-id="6cf6e-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-130">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="6cf6e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf6e-131">CommonParameters</span></span>
<span data-ttu-id="6cf6e-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf6e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf6e-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cf6e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf6e-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6cf6e-134">INPUTS</span></span>

### <span data-ttu-id="6cf6e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6cf6e-135">System.String</span></span>

## <span data-ttu-id="6cf6e-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6cf6e-136">OUTPUTS</span></span>

### <span data-ttu-id="6cf6e-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="6cf6e-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="6cf6e-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6cf6e-138">NOTES</span></span>

## <span data-ttu-id="6cf6e-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6cf6e-139">RELATED LINKS</span></span>

[<span data-ttu-id="6cf6e-140">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6cf6e-140">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


