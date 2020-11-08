---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 20e0c403656cc7fd714981f73b2a5a8c1335f9b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009564"
---
# <span data-ttu-id="2b1d1-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2b1d1-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="2b1d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1d1-103">Hebt die Registrierung eines Windows-Servers oder eines anderen Containers aus dem Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="2b1d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b1d1-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b1d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="2b1d1-106">Das Cmdlet " **Unregister-AzRecoveryServicesBackupContainer** " hebt die Registrierung eines Windows-Servers oder eines anderen Sicherungs Containers aus dem Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="2b1d1-107">Dieses Cmdlet entfernt Verweise auf einen Container aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="2b1d1-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="2b1d1-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="2b1d1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b1d1-110">EXAMPLES</span></span>

### <span data-ttu-id="2b1d1-111">Beispiel 1: Aufheben der Registrierung eines Windows-Servers aus dem Tresor</span><span class="sxs-lookup"><span data-stu-id="2b1d1-111">Example 1: Unregister a Windows Server from the vault</span></span>
```powershell
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="2b1d1-112">Der erste Befehl ruft den Windows-Container mit dem Namen Server01.contoso.com ab, der im Tresor registriert ist, und speichert ihn dann in der $cont-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="2b1d1-113">Der zweite Befehl hebt die Registrierung des angegebenen Windows-Servers aus dem Azure Backup Vault auf.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="2b1d1-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2b1d1-114">Example 2</span></span>

<span data-ttu-id="2b1d1-115">Hebt die Registrierung eines Windows-Servers oder eines anderen Containers aus dem Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-115">Unregisters a Windows Server or other container from the vault.</span></span> <span data-ttu-id="2b1d1-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="2b1d1-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupContainer -Container $Cont -VaultId $vault.ID
```

## <span data-ttu-id="2b1d1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b1d1-117">PARAMETERS</span></span>

### <span data-ttu-id="2b1d1-118">-Container</span><span class="sxs-lookup"><span data-stu-id="2b1d1-118">-Container</span></span>
<span data-ttu-id="2b1d1-119">Gibt ein Backup-Containerobjekt an, um die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-119">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="2b1d1-120">Verwenden Sie das Get-AzRecoveryServicesBackupContainer-Cmdlet, um ein **BackupContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-120">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="2b1d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1d1-121">-DefaultProfile</span></span>
<span data-ttu-id="2b1d1-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b1d1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b1d1-123">-PassThru</span></span>
<span data-ttu-id="2b1d1-124">Geben Sie den zu löschenden Container zurück.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-124">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="2b1d1-125">-Tresor</span><span class="sxs-lookup"><span data-stu-id="2b1d1-125">-VaultId</span></span>
<span data-ttu-id="2b1d1-126">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="2b1d1-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2b1d1-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b1d1-127">-Confirm</span></span>
<span data-ttu-id="2b1d1-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b1d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b1d1-129">-WhatIf</span></span>
<span data-ttu-id="2b1d1-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-130">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="2b1d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1d1-131">CommonParameters</span></span>
<span data-ttu-id="2b1d1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b1d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1d1-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b1d1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1d1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b1d1-134">INPUTS</span></span>

### <span data-ttu-id="2b1d1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2b1d1-135">System.String</span></span>

## <span data-ttu-id="2b1d1-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b1d1-136">OUTPUTS</span></span>

### <span data-ttu-id="2b1d1-137">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="2b1d1-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="2b1d1-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b1d1-138">NOTES</span></span>

## <span data-ttu-id="2b1d1-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b1d1-139">RELATED LINKS</span></span>

[<span data-ttu-id="2b1d1-140">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2b1d1-140">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


