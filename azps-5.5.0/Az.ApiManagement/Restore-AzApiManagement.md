---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164385"
---
# <span data-ttu-id="c6666-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6666-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="c6666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6666-102">SYNOPSIS</span></span>
<span data-ttu-id="c6666-103">Stellt einen API-Verwaltungsdienst aus dem angegebenen Azure-Speicher-BLOB wieder bereit.</span><span class="sxs-lookup"><span data-stu-id="c6666-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="c6666-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6666-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6666-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6666-105">DESCRIPTION</span></span>
<span data-ttu-id="c6666-106">Das **Cmdlet "Restore-AzApiManagement"** stellt einen API-Verwaltungsdienst aus der angegebenen Sicherung wieder her, die sich in einem Azurestorage-BLOB befinden.</span><span class="sxs-lookup"><span data-stu-id="c6666-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="c6666-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c6666-107">EXAMPLES</span></span>

### <span data-ttu-id="c6666-108">Beispiel 1: Wiederherstellen eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="c6666-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="c6666-109">Mit diesem Befehl wird ein API-Verwaltungsdienst aus dem Azure-Speicher-BLOB wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="c6666-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="c6666-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6666-110">PARAMETERS</span></span>

### <span data-ttu-id="c6666-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6666-111">-DefaultProfile</span></span>
<span data-ttu-id="c6666-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c6666-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6666-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c6666-113">-Name</span></span>
<span data-ttu-id="c6666-114">Gibt den Namen der API-Verwaltungsinstanz an, die mit der Sicherung wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c6666-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="c6666-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6666-115">-PassThru</span></span>
<span data-ttu-id="c6666-116">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c6666-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c6666-117">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c6666-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6666-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6666-118">-ResourceGroupName</span></span>
<span data-ttu-id="c6666-119">Gibt den Namen der Ressourcengruppe an, unter der die API Management (API-Verwaltung) vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c6666-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="c6666-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="c6666-120">-SourceBlobName</span></span>
<span data-ttu-id="c6666-121">Gibt den Namen des Azure Storage Backup Source BLOB an.</span><span class="sxs-lookup"><span data-stu-id="c6666-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="c6666-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="c6666-122">-SourceContainerName</span></span>
<span data-ttu-id="c6666-123">Gibt den Namen des Azure Storage Backup Source Containers an.</span><span class="sxs-lookup"><span data-stu-id="c6666-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="c6666-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c6666-124">-StorageContext</span></span>
<span data-ttu-id="c6666-125">Gibt den Kontext der Speicherverbindung an.</span><span class="sxs-lookup"><span data-stu-id="c6666-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="c6666-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6666-126">CommonParameters</span></span>
<span data-ttu-id="c6666-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6666-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6666-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6666-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6666-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c6666-129">INPUTS</span></span>

### <span data-ttu-id="c6666-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c6666-130">System.String</span></span>

## <span data-ttu-id="c6666-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c6666-131">OUTPUTS</span></span>

### <span data-ttu-id="c6666-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6666-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c6666-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c6666-133">NOTES</span></span>

## <span data-ttu-id="c6666-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c6666-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6666-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6666-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="c6666-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6666-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="c6666-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6666-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="c6666-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c6666-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


