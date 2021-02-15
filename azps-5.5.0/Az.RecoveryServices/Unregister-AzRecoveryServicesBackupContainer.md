---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 20e0c403656cc7fd714981f73b2a5a8c1335f9b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151105"
---
# <span data-ttu-id="1224b-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1224b-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="1224b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1224b-102">SYNOPSIS</span></span>
<span data-ttu-id="1224b-103">Die Registrierung eines Windows Server- oder anderen Containers aus dem Tresor wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1224b-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="1224b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1224b-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1224b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1224b-105">DESCRIPTION</span></span>
<span data-ttu-id="1224b-106">Das **Cmdlet "Unregister-AzRecoveryServicesBackupContainer"** entfernt die Registrierung eines Windows Server- oder anderen Sicherungscontainers aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="1224b-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="1224b-107">Dieses Cmdlet entfernt Verweise auf einen Container aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="1224b-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="1224b-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle mit diesem Container verknüpften geschützten Daten löschen.</span><span class="sxs-lookup"><span data-stu-id="1224b-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="1224b-109">Legen Sie den Tresorkontext mithilfe des cmdlets Set-AzRecoveryServicesVaultContext, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="1224b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1224b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1224b-110">EXAMPLES</span></span>

### <span data-ttu-id="1224b-111">Beispiel 1: Aufheben der Registrierung eines Windows Server aus dem Tresor</span><span class="sxs-lookup"><span data-stu-id="1224b-111">Example 1: Unregister a Windows Server from the vault</span></span>
```powershell
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="1224b-112">Der erste Befehl ruft den im Tresor registrierten server01.contoso.com A0 ab und speichert ihn dann in der $Cont Variable.</span><span class="sxs-lookup"><span data-stu-id="1224b-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="1224b-113">Mit dem zweiten Befehl wird die Registrierung des angegebenen Windows Server aus dem Azure Backup Vault aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1224b-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="1224b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1224b-114">Example 2</span></span>

<span data-ttu-id="1224b-115">Die Registrierung eines Windows Server- oder anderen Containers aus dem Tresor wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1224b-115">Unregisters a Windows Server or other container from the vault.</span></span> <span data-ttu-id="1224b-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="1224b-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupContainer -Container $Cont -VaultId $vault.ID
```

## <span data-ttu-id="1224b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1224b-117">PARAMETERS</span></span>

### <span data-ttu-id="1224b-118">-Container</span><span class="sxs-lookup"><span data-stu-id="1224b-118">-Container</span></span>
<span data-ttu-id="1224b-119">Gibt ein Sicherungscontainerobjekt an, das die Registrierung aufheben soll.</span><span class="sxs-lookup"><span data-stu-id="1224b-119">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="1224b-120">Verwenden Sie **zum** Abrufen eines Sicherungscontainerobjekts das Get-AzRecoveryServicesBackupContainer Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1224b-120">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="1224b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1224b-121">-DefaultProfile</span></span>
<span data-ttu-id="1224b-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1224b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1224b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1224b-123">-PassThru</span></span>
<span data-ttu-id="1224b-124">Geben Sie den zu löschende Container zurück.</span><span class="sxs-lookup"><span data-stu-id="1224b-124">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="1224b-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1224b-125">-VaultId</span></span>
<span data-ttu-id="1224b-126">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="1224b-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="1224b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1224b-127">-Confirm</span></span>
<span data-ttu-id="1224b-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1224b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1224b-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1224b-129">-WhatIf</span></span>
<span data-ttu-id="1224b-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1224b-130">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="1224b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1224b-131">CommonParameters</span></span>
<span data-ttu-id="1224b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1224b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1224b-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1224b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1224b-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1224b-134">INPUTS</span></span>

### <span data-ttu-id="1224b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1224b-135">System.String</span></span>

## <span data-ttu-id="1224b-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1224b-136">OUTPUTS</span></span>

### <span data-ttu-id="1224b-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="1224b-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="1224b-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1224b-138">NOTES</span></span>

## <span data-ttu-id="1224b-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1224b-139">RELATED LINKS</span></span>

[<span data-ttu-id="1224b-140">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="1224b-140">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


