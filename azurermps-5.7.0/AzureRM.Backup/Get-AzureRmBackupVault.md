---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664698"
---
# <span data-ttu-id="5c25d-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="5c25d-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="5c25d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c25d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c25d-103">Ruft Sicherungs Depots ab.</span><span class="sxs-lookup"><span data-stu-id="5c25d-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c25d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c25d-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c25d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c25d-105">DESCRIPTION</span></span>
<span data-ttu-id="5c25d-106">Das Cmdlet " **Get-AzureRmBackupVault** " ruft Azure Backup Vaults ab.</span><span class="sxs-lookup"><span data-stu-id="5c25d-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="5c25d-107">Dieses Cmdlet gibt **AzureRmBackupVault** -Objekte zur Verwendung mit anderen Cmdlets zurück.</span><span class="sxs-lookup"><span data-stu-id="5c25d-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="5c25d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c25d-108">EXAMPLES</span></span>

### <span data-ttu-id="5c25d-109">Beispiel 1: Anzeigen aller Sicherungs Depots</span><span class="sxs-lookup"><span data-stu-id="5c25d-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="5c25d-110">Dieser Befehl ruft alle Azure Backup Vaults ab.</span><span class="sxs-lookup"><span data-stu-id="5c25d-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="5c25d-111">Beispiel 2: Anzeigen aller in West-US erstellten Tresore</span><span class="sxs-lookup"><span data-stu-id="5c25d-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="5c25d-112">Dieser Befehl ruft alle Sicherungs Depots ab.</span><span class="sxs-lookup"><span data-stu-id="5c25d-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="5c25d-113">Der Befehl übergibt Sie mithilfe des Pipelineoperators an das Where-Object-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c25d-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5c25d-114">Dieses Cmdlet filtert die Ergebnisse basierend auf der **Region** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5c25d-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="5c25d-115">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="5c25d-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="5c25d-116">Beispiel 3: Abrufen eines bestimmten Tresors</span><span class="sxs-lookup"><span data-stu-id="5c25d-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="5c25d-117">Dieser Befehl ruft den Tresor mit dem Namen Vault03 ab.</span><span class="sxs-lookup"><span data-stu-id="5c25d-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="5c25d-118">Beispiel 4: zählen der Anzahl von Tresoren, die über lokal redundanten Speicher verfügen</span><span class="sxs-lookup"><span data-stu-id="5c25d-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="5c25d-119">Dieser Befehl ruft alle Azure Backup Vaults ab.</span><span class="sxs-lookup"><span data-stu-id="5c25d-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="5c25d-120">Der Befehl übergibt sie an **Where-Object** , wodurch die Ergebnisse basierend auf der **Speicher** Eigenschaft gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="5c25d-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="5c25d-121">Der Befehl übergibt diejenigen, die einen Wert von LocallyRedundant haben, an das Measure-Object-Cmdlet, in dem die Ergebnisse gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="5c25d-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="5c25d-122">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="5c25d-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="5c25d-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c25d-123">PARAMETERS</span></span>

### <span data-ttu-id="5c25d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c25d-124">-DefaultProfile</span></span>
<span data-ttu-id="5c25d-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5c25d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c25d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5c25d-126">-Name</span></span>
<span data-ttu-id="5c25d-127">Gibt den Namen des Sicherungsspeichers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5c25d-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="5c25d-128">Wenn mehr als ein Backup Vault denselben Namen hat, gibt dieses Cmdlet alle zurück.</span><span class="sxs-lookup"><span data-stu-id="5c25d-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="5c25d-129">Geben Sie den *ResourceGroupName* -Parameter an, um einen eindeutigen Tresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5c25d-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c25d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c25d-130">-ResourceGroupName</span></span>
<span data-ttu-id="5c25d-131">Gibt den Namen einer Azure-Ressourcengruppe an, in der dieses Cmdlet einen Sicherungsspeicher erhält.</span><span class="sxs-lookup"><span data-stu-id="5c25d-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c25d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c25d-132">CommonParameters</span></span>
<span data-ttu-id="5c25d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c25d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c25d-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c25d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c25d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c25d-135">INPUTS</span></span>

### <span data-ttu-id="5c25d-136">Keine</span><span class="sxs-lookup"><span data-stu-id="5c25d-136">None</span></span>
<span data-ttu-id="5c25d-137">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5c25d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c25d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c25d-138">OUTPUTS</span></span>

### <span data-ttu-id="5c25d-139">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="5c25d-139">AzureRmBackupVault</span></span>

## <span data-ttu-id="5c25d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c25d-140">NOTES</span></span>
* <span data-ttu-id="5c25d-141">Keine</span><span class="sxs-lookup"><span data-stu-id="5c25d-141">None</span></span>

## <span data-ttu-id="5c25d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c25d-142">RELATED LINKS</span></span>

[<span data-ttu-id="5c25d-143">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="5c25d-143">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="5c25d-144">Neu – AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="5c25d-144">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="5c25d-145">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="5c25d-145">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="5c25d-146">Satz-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="5c25d-146">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


