---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 8530dbff2e348f1b068afe7293cae9c993ce064e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497917"
---
# <span data-ttu-id="a207e-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a207e-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="a207e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a207e-102">SYNOPSIS</span></span>
<span data-ttu-id="a207e-103">Löscht einen Sicherungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a207e-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a207e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a207e-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a207e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a207e-105">DESCRIPTION</span></span>
<span data-ttu-id="a207e-106">Mit dem Cmdlet **Remove-AzureRmBackupVault** wird ein Azure Backup Vault gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a207e-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="a207e-107">Bevor Sie ein Sicherungs Depot löschen können, muss es leer sein.</span><span class="sxs-lookup"><span data-stu-id="a207e-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="a207e-108">Verwenden Sie das Cmdlet " **Remove-AzureRmBackupContainer** ", um die Backup-Daten des virtuellen Computers Infrastructure as a Service (IaaS) aus dem Tresor zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a207e-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="a207e-109">Verwenden Sie das Cmdlet **delete-registeredserver** , um andere registrierte Server und Sicherungsdaten zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="a207e-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="a207e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a207e-110">EXAMPLES</span></span>

### <span data-ttu-id="a207e-111">Beispiel 1: Löschen eines Azure-Sicherungsspeichers</span><span class="sxs-lookup"><span data-stu-id="a207e-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="a207e-112">Dieser Befehl ruft das Azure Backup Vault mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="a207e-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="a207e-113">Der Befehl übergibt diesen Tresor mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a207e-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a207e-114">Das aktuelle Cmdlet entfernt den Tresor.</span><span class="sxs-lookup"><span data-stu-id="a207e-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="a207e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a207e-115">PARAMETERS</span></span>

### <span data-ttu-id="a207e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a207e-116">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a207e-117">-Vault</span><span class="sxs-lookup"><span data-stu-id="a207e-117">-Vault</span></span>
<span data-ttu-id="a207e-118">Gibt einen sicherungstresor an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="a207e-118">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="a207e-119">Verwenden Sie zum Abrufen eines **AzureRmBackupVault** das Get-AzureRmBackupVault-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a207e-119">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="a207e-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a207e-120">-Confirm</span></span>
<span data-ttu-id="a207e-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a207e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a207e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a207e-122">-WhatIf</span></span>
<span data-ttu-id="a207e-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a207e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a207e-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a207e-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a207e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a207e-125">-DefaultProfile</span></span>
<span data-ttu-id="a207e-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a207e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a207e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a207e-127">CommonParameters</span></span>
<span data-ttu-id="a207e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a207e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a207e-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a207e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a207e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a207e-130">INPUTS</span></span>

### <span data-ttu-id="a207e-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="a207e-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="a207e-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a207e-132">OUTPUTS</span></span>

### <span data-ttu-id="a207e-133">Keine</span><span class="sxs-lookup"><span data-stu-id="a207e-133">None</span></span>

## <span data-ttu-id="a207e-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="a207e-134">NOTES</span></span>
* <span data-ttu-id="a207e-135">Keine</span><span class="sxs-lookup"><span data-stu-id="a207e-135">None</span></span>

## <span data-ttu-id="a207e-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a207e-136">RELATED LINKS</span></span>

[<span data-ttu-id="a207e-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a207e-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="a207e-138">Neu – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a207e-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="a207e-139">Satz-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a207e-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


