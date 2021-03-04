---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d1c7e1938d50e4a970dbec15568bc5cf10257639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946355"
---
# <span data-ttu-id="83182-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="83182-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="83182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83182-102">SYNOPSIS</span></span>
<span data-ttu-id="83182-103">Stellt einen API-Verwaltungsdienst aus dem angegebenen Azure-Speicherblob wieder bereit.</span><span class="sxs-lookup"><span data-stu-id="83182-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="83182-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83182-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83182-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83182-105">DESCRIPTION</span></span>
<span data-ttu-id="83182-106">Das **Cmdlet Restore-AzApiManagement** stellt einen API-Verwaltungsdienst aus der angegebenen Sicherung wieder her, die sich in einem Azurestorage-Blob befinden.</span><span class="sxs-lookup"><span data-stu-id="83182-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="83182-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83182-107">EXAMPLES</span></span>

### <span data-ttu-id="83182-108">Beispiel 1: Wiederherstellen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="83182-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="83182-109">Mit diesem Befehl wird ein API-Verwaltungsdienst aus dem Azure-Speicherblob wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="83182-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="83182-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="83182-110">PARAMETERS</span></span>

### <span data-ttu-id="83182-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83182-111">-DefaultProfile</span></span>
<span data-ttu-id="83182-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="83182-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83182-113">-Name</span><span class="sxs-lookup"><span data-stu-id="83182-113">-Name</span></span>
<span data-ttu-id="83182-114">Gibt den Namen der API-Verwaltungsinstanz an, die mit der Sicherung wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="83182-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="83182-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83182-115">-PassThru</span></span>
<span data-ttu-id="83182-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="83182-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="83182-117">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="83182-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83182-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83182-118">-ResourceGroupName</span></span>
<span data-ttu-id="83182-119">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="83182-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="83182-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="83182-120">-SourceBlobName</span></span>
<span data-ttu-id="83182-121">Gibt den Namen des Azure-Speichersicherungsquellenblobs an.</span><span class="sxs-lookup"><span data-stu-id="83182-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="83182-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="83182-122">-SourceContainerName</span></span>
<span data-ttu-id="83182-123">Gibt den Namen des Azure-Speichersicherungsquellencontainers an.</span><span class="sxs-lookup"><span data-stu-id="83182-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="83182-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="83182-124">-StorageContext</span></span>
<span data-ttu-id="83182-125">Gibt den Speicherverbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="83182-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="83182-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83182-126">CommonParameters</span></span>
<span data-ttu-id="83182-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83182-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83182-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83182-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83182-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83182-129">INPUTS</span></span>

### <span data-ttu-id="83182-130">System.String</span><span class="sxs-lookup"><span data-stu-id="83182-130">System.String</span></span>

## <span data-ttu-id="83182-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83182-131">OUTPUTS</span></span>

### <span data-ttu-id="83182-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="83182-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="83182-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="83182-133">NOTES</span></span>

## <span data-ttu-id="83182-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="83182-134">RELATED LINKS</span></span>

[<span data-ttu-id="83182-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="83182-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="83182-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="83182-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="83182-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="83182-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="83182-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="83182-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


