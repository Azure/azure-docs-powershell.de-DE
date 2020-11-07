---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662282"
---
# <span data-ttu-id="eb6c5-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6c5-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="eb6c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb6c5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb6c5-103">Stellt einen API-Verwaltungsdienst aus dem angegebenen Azure Storage-BLOB wieder her.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb6c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb6c5-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb6c5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb6c5-105">DESCRIPTION</span></span>
<span data-ttu-id="eb6c5-106">Das Cmdlet **Restore-AzureRmApiManagement** stellt einen API-Verwaltungsdienst aus der angegebenen Sicherung wieder her, die sich in einem Azurestorage-BLOB befindet.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="eb6c5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb6c5-107">EXAMPLES</span></span>

### <span data-ttu-id="eb6c5-108">Beispiel 1: Wiederherstellen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="eb6c5-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="eb6c5-109">Mit diesem Befehl wird ein API-Verwaltungsdienst aus dem Azure Storage-BLOB wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="eb6c5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb6c5-110">PARAMETERS</span></span>

### <span data-ttu-id="eb6c5-111">-Name</span><span class="sxs-lookup"><span data-stu-id="eb6c5-111">-Name</span></span>
<span data-ttu-id="eb6c5-112">Gibt den Namen der API-Verwaltungsinstanz an, die mit der Sicherung wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="eb6c5-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb6c5-113">-PassThru</span></span>
<span data-ttu-id="eb6c5-114">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb6c5-115">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb6c5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb6c5-116">-ResourceGroupName</span></span>
<span data-ttu-id="eb6c5-117">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-117">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="eb6c5-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="eb6c5-118">-SourceBlobName</span></span>
<span data-ttu-id="eb6c5-119">Gibt den Namen des Azure Storage-Backup-Quell-BLOB an.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-119">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="eb6c5-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="eb6c5-120">-SourceContainerName</span></span>
<span data-ttu-id="eb6c5-121">Gibt den Namen des Azure Storage-Sicherungs Quellcontainers an.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-121">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="eb6c5-122">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="eb6c5-122">-StorageContext</span></span>
<span data-ttu-id="eb6c5-123">Gibt den Speicher Verbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-123">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="eb6c5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb6c5-124">-DefaultProfile</span></span>
<span data-ttu-id="eb6c5-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb6c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb6c5-126">CommonParameters</span></span>
<span data-ttu-id="eb6c5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb6c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb6c5-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb6c5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb6c5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb6c5-129">INPUTS</span></span>

## <span data-ttu-id="eb6c5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb6c5-130">OUTPUTS</span></span>

### <span data-ttu-id="eb6c5-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6c5-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="eb6c5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb6c5-132">NOTES</span></span>

## <span data-ttu-id="eb6c5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb6c5-133">RELATED LINKS</span></span>

[<span data-ttu-id="eb6c5-134">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6c5-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="eb6c5-135">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6c5-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="eb6c5-136">Neu – AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6c5-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="eb6c5-137">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb6c5-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


