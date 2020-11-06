---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: 6ad62049600f1734beabcc1a322086aad1a92348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498901"
---
# <span data-ttu-id="0ab51-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0ab51-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="0ab51-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ab51-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab51-103">Hebt die Registrierung eines Windows-Servers oder eines anderen Containers aus dem Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="0ab51-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ab51-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ab51-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ab51-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ab51-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab51-106">Das Cmdlet " **Unregister-AzureRmRecoveryServicesBackupContainer** " hebt die Registrierung eines Windows-Servers oder eines anderen Sicherungs Containers aus dem Tresor auf.</span><span class="sxs-lookup"><span data-stu-id="0ab51-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="0ab51-107">Dieses Cmdlet entfernt Verweise auf einen Container aus dem Tresor.</span><span class="sxs-lookup"><span data-stu-id="0ab51-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="0ab51-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0ab51-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="0ab51-109">Setzen Sie den Vault-Kontext mithilfe des Set-AzureRmRecoveryServicesVaultContext-Cmdlets, bevor Sie das aktuelle Cmdlet verwenden.</span><span class="sxs-lookup"><span data-stu-id="0ab51-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0ab51-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ab51-110">EXAMPLES</span></span>

### <span data-ttu-id="0ab51-111">Beispiel 1: Aufheben der Registrierung eines Windows-Servers aus dem Tresor</span><span class="sxs-lookup"><span data-stu-id="0ab51-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="0ab51-112">Der erste Befehl ruft den Windows-Container mit dem Namen Server01.contoso.com ab, der im Tresor registriert ist, und speichert ihn dann in der $cont-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0ab51-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="0ab51-113">Der zweite Befehl hebt die Registrierung des angegebenen Windows-Servers aus dem Azure Backup Vault auf.</span><span class="sxs-lookup"><span data-stu-id="0ab51-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="0ab51-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ab51-114">PARAMETERS</span></span>

### <span data-ttu-id="0ab51-115">-Container</span><span class="sxs-lookup"><span data-stu-id="0ab51-115">-Container</span></span>
<span data-ttu-id="0ab51-116">Gibt ein Backup-Containerobjekt an, um die Registrierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="0ab51-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="0ab51-117">Verwenden Sie das Get-AzureRmRecoveryServicesBackupContainer-Cmdlet, um ein **BackupContainer** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ab51-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab51-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab51-118">-DefaultProfile</span></span>
<span data-ttu-id="0ab51-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ab51-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ab51-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0ab51-120">-PassThru</span></span>
<span data-ttu-id="0ab51-121">Geben Sie den zu löschenden Container zurück.</span><span class="sxs-lookup"><span data-stu-id="0ab51-121">Return the container to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab51-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0ab51-122">-Confirm</span></span>
<span data-ttu-id="0ab51-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0ab51-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab51-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ab51-124">-WhatIf</span></span>
<span data-ttu-id="0ab51-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ab51-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ab51-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ab51-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ab51-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab51-127">CommonParameters</span></span>
<span data-ttu-id="0ab51-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab51-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab51-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab51-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab51-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ab51-130">INPUTS</span></span>

### <span data-ttu-id="0ab51-131">Keine</span><span class="sxs-lookup"><span data-stu-id="0ab51-131">None</span></span>
<span data-ttu-id="0ab51-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0ab51-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ab51-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ab51-133">OUTPUTS</span></span>

## <span data-ttu-id="0ab51-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ab51-134">NOTES</span></span>

## <span data-ttu-id="0ab51-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ab51-135">RELATED LINKS</span></span>

[<span data-ttu-id="0ab51-136">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0ab51-136">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


