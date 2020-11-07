---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: 0fd004cdb727a0e665fd9b867854b3b8e4054c9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665338"
---
# <span data-ttu-id="1ccf5-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ccf5-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="1ccf5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ccf5-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccf5-103">Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="1ccf5-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ccf5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ccf5-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ccf5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ccf5-105">DESCRIPTION</span></span>
<span data-ttu-id="1ccf5-106">Mit dem Cmdlet " **Backup-AzureRmApiManagement** " wird eine Instanz eines Azure API-Verwaltungsdiensts gesichert.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="1ccf5-107">Dieses Cmdlet speichert die Sicherung als Azure-Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="1ccf5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ccf5-108">EXAMPLES</span></span>

### <span data-ttu-id="1ccf5-109">Beispiel 1: Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="1ccf5-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="1ccf5-110">Mit diesem Befehl wird ein API-Verwaltungsdienst zu einem Speicher-BLOB gesichert.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="1ccf5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ccf5-111">PARAMETERS</span></span>

### <span data-ttu-id="1ccf5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccf5-112">-DefaultProfile</span></span>
<span data-ttu-id="1ccf5-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1ccf5-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1ccf5-114">-Name</span></span>
<span data-ttu-id="1ccf5-115">Gibt den Namen der API-Verwaltungs Bereitstellung an, die von diesem Cmdlet gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf5-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ccf5-116">-PassThru</span></span>
<span data-ttu-id="1ccf5-117">Gibt an, dass dieses Cmdlet das gesicherte **PsApiManagement** -Objekt zurückgibt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="1ccf5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ccf5-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ccf5-119">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf5-120">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="1ccf5-120">-StorageContext</span></span>
<span data-ttu-id="1ccf5-121">Gibt einen Speicher Verbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-121">Specifies a storage connection context.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf5-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="1ccf5-122">-TargetBlobName</span></span>
<span data-ttu-id="1ccf5-123">Gibt den Namen des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="1ccf5-124">Wenn das BLOB nicht vorhanden ist, wird es von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="1ccf5-125">Dieses Cmdlet generiert einen Standardwert auf der Grundlage des folgenden Musters:</span><span class="sxs-lookup"><span data-stu-id="1ccf5-125">This cmdlet generates a default value based on the following pattern:</span></span> 

<span data-ttu-id="1ccf5-126">{Name}-{yyyy-mm-dd-hh-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="1ccf5-126">{Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf5-127">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="1ccf5-127">-TargetContainerName</span></span>
<span data-ttu-id="1ccf5-128">Gibt den Namen des Containers des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-128">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="1ccf5-129">Wenn der Container nicht vorhanden ist, wird er von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-129">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccf5-130">CommonParameters</span></span>
<span data-ttu-id="1ccf5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccf5-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ccf5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccf5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ccf5-133">INPUTS</span></span>

### <span data-ttu-id="1ccf5-134">Keine</span><span class="sxs-lookup"><span data-stu-id="1ccf5-134">None</span></span>
<span data-ttu-id="1ccf5-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1ccf5-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ccf5-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ccf5-136">OUTPUTS</span></span>

### <span data-ttu-id="1ccf5-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ccf5-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1ccf5-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ccf5-138">NOTES</span></span>

## <span data-ttu-id="1ccf5-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ccf5-139">RELATED LINKS</span></span>

[<span data-ttu-id="1ccf5-140">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ccf5-140">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="1ccf5-141">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ccf5-141">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="1ccf5-142">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ccf5-142">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="1ccf5-143">Wiederherstellen – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1ccf5-143">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


