---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/restore-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 1fc22563949f44882d0b6ed1f864d217faacff9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501237"
---
# <span data-ttu-id="1005b-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1005b-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="1005b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1005b-102">SYNOPSIS</span></span>
<span data-ttu-id="1005b-103">Stellt einen API-Verwaltungsdienst aus dem angegebenen Azure Storage-BLOB wieder her.</span><span class="sxs-lookup"><span data-stu-id="1005b-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1005b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1005b-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1005b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1005b-105">DESCRIPTION</span></span>
<span data-ttu-id="1005b-106">Das Cmdlet **Restore-AzureRmApiManagement** stellt einen API-Verwaltungsdienst aus der angegebenen Sicherung wieder her, die sich in einem Azurestorage-BLOB befindet.</span><span class="sxs-lookup"><span data-stu-id="1005b-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="1005b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1005b-107">EXAMPLES</span></span>

### <span data-ttu-id="1005b-108">Beispiel 1: Wiederherstellen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="1005b-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="1005b-109">Mit diesem Befehl wird ein API-Verwaltungsdienst aus dem Azure Storage-BLOB wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="1005b-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="1005b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1005b-110">PARAMETERS</span></span>

### <span data-ttu-id="1005b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1005b-111">-DefaultProfile</span></span>
<span data-ttu-id="1005b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1005b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1005b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1005b-113">-Name</span></span>
<span data-ttu-id="1005b-114">Gibt den Namen der API-Verwaltungsinstanz an, die mit der Sicherung wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1005b-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1005b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1005b-115">-PassThru</span></span>
<span data-ttu-id="1005b-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1005b-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1005b-117">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="1005b-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1005b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1005b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1005b-119">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1005b-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1005b-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="1005b-120">-SourceBlobName</span></span>
<span data-ttu-id="1005b-121">Gibt den Namen des Azure Storage-Backup-Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="1005b-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1005b-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="1005b-122">-SourceContainerName</span></span>
<span data-ttu-id="1005b-123">Gibt den Namen des Azure Storage-Sicherungs Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="1005b-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1005b-124">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="1005b-124">-StorageContext</span></span>
<span data-ttu-id="1005b-125">Gibt den Speicher Verbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="1005b-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1005b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1005b-126">CommonParameters</span></span>
<span data-ttu-id="1005b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1005b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1005b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1005b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1005b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1005b-129">INPUTS</span></span>

### <span data-ttu-id="1005b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1005b-130">System.String</span></span>

## <span data-ttu-id="1005b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1005b-131">OUTPUTS</span></span>

### <span data-ttu-id="1005b-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1005b-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1005b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1005b-133">NOTES</span></span>

## <span data-ttu-id="1005b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1005b-134">RELATED LINKS</span></span>

[<span data-ttu-id="1005b-135">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1005b-135">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="1005b-136">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1005b-136">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="1005b-137">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1005b-137">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="1005b-138">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1005b-138">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


