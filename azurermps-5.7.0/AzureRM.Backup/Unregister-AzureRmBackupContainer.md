---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 059db3658f97a28bda8960384aef4300595dca20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665315"
---
# <span data-ttu-id="9c62c-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9c62c-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="9c62c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9c62c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c62c-103">Hebt die Registrierung eines Containers aus einem sicherungstresor auf.</span><span class="sxs-lookup"><span data-stu-id="9c62c-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c62c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c62c-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c62c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c62c-105">DESCRIPTION</span></span>
<span data-ttu-id="9c62c-106">Das Cmdlet " **Unregister-AzureRmBackupContainer** " hebt die Registrierung des Windows Server-oder Azure Virtual Machine aus einem Azure Backup Vault auf.</span><span class="sxs-lookup"><span data-stu-id="9c62c-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="9c62c-107">Dieses Cmdlet entfernt Verweise auf einen Container aus dem Sicherungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9c62c-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="9c62c-108">Bevor Sie die Registrierung eines Containers aufheben können, müssen Sie alle geschützten Daten löschen, die diesem Container zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9c62c-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="9c62c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9c62c-109">EXAMPLES</span></span>

### <span data-ttu-id="9c62c-110">Beispiel 1: Aufheben der Registrierung eines Windows-Servers</span><span class="sxs-lookup"><span data-stu-id="9c62c-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="9c62c-111">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mithilfe des Get-AzureRmBackupVault-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="9c62c-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="9c62c-112">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="9c62c-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9c62c-113">Der zweite Befehl ruft mithilfe des Get-AzureRmBackupContainer-Cmdlets einen Container ab, der den angegebenen Namen im Tresor in $Vault aufweist.</span><span class="sxs-lookup"><span data-stu-id="9c62c-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="9c62c-114">Der Befehl speichert das Objekt in der $Container Variablen.</span><span class="sxs-lookup"><span data-stu-id="9c62c-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="9c62c-115">Der endgültige Befehl hebt die Registrierung des angegebenen Windows-Servers aus dem Azure Backup Vault auf.</span><span class="sxs-lookup"><span data-stu-id="9c62c-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="9c62c-116">Beispiel 2: Aufheben der Registrierung eines Windows-Servers ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="9c62c-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="9c62c-117">Dieser Befehl hebt die Registrierung des angegebenen Windows-Servers aus dem Azure Backup Vault auf, genau wie im ersten Beispiel.</span><span class="sxs-lookup"><span data-stu-id="9c62c-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="9c62c-118">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="9c62c-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9c62c-119">Daher werden Sie vom Befehl nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="9c62c-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9c62c-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c62c-120">PARAMETERS</span></span>

### <span data-ttu-id="9c62c-121">-Container</span><span class="sxs-lookup"><span data-stu-id="9c62c-121">-Container</span></span>
<span data-ttu-id="9c62c-122">Gibt den Windows-Server oder Azure Virtual Machine an, die von diesem Cmdlet aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="9c62c-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="9c62c-123">Verwenden Sie zum Abrufen eines **AzureRmBackupContainer** das Get-AzureRmBackupContainer-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c62c-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c62c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c62c-124">-DefaultProfile</span></span>
<span data-ttu-id="9c62c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9c62c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c62c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9c62c-126">-Force</span></span>
<span data-ttu-id="9c62c-127">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9c62c-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="9c62c-128">Dieser Parameter ist nur für **AzureBackupContainer** -Objekte des Typs Windows relevant.</span><span class="sxs-lookup"><span data-stu-id="9c62c-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c62c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9c62c-129">-Confirm</span></span>
<span data-ttu-id="9c62c-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c62c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c62c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c62c-131">-WhatIf</span></span>
<span data-ttu-id="9c62c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9c62c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c62c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c62c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c62c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c62c-134">CommonParameters</span></span>
<span data-ttu-id="9c62c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c62c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c62c-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c62c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c62c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9c62c-137">INPUTS</span></span>

### <span data-ttu-id="9c62c-138">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9c62c-138">AzureBackupContainer</span></span>

## <span data-ttu-id="9c62c-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9c62c-139">OUTPUTS</span></span>

### <span data-ttu-id="9c62c-140">AzureBackupJob</span><span class="sxs-lookup"><span data-stu-id="9c62c-140">AzureBackupJob</span></span>
<span data-ttu-id="9c62c-141">Dieses Cmdlet gibt $NULL zurück, wenn es sich bei dem Containertyp um Windows Server handelt.</span><span class="sxs-lookup"><span data-stu-id="9c62c-141">This cmdlet returns $Null if the container type is Windows Server.</span></span>

## <span data-ttu-id="9c62c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="9c62c-142">NOTES</span></span>
* <span data-ttu-id="9c62c-143">Keine</span><span class="sxs-lookup"><span data-stu-id="9c62c-143">None</span></span>

## <span data-ttu-id="9c62c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9c62c-144">RELATED LINKS</span></span>

[<span data-ttu-id="9c62c-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9c62c-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="9c62c-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9c62c-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="9c62c-147">Registrieren-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9c62c-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


