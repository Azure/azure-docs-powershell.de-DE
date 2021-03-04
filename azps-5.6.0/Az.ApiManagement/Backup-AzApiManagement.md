---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 1f0ceb4f349e7fdfee38837561dc436c16cd451b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939035"
---
# <span data-ttu-id="dd073-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd073-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="dd073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd073-102">SYNOPSIS</span></span>
<span data-ttu-id="dd073-103">Unterstützt einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="dd073-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="dd073-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd073-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd073-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd073-105">DESCRIPTION</span></span>
<span data-ttu-id="dd073-106">Das **Cmdlet Backup-AzApiManagement** unterstützt eine Instanz eines Azure API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="dd073-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="dd073-107">Dieses Cmdlet speichert die Sicherung als Azure Storage-Blob.</span><span class="sxs-lookup"><span data-stu-id="dd073-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="dd073-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd073-108">EXAMPLES</span></span>

### <span data-ttu-id="dd073-109">Beispiel 1: Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="dd073-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="dd073-110">Mit diesem Befehl wird ein API-Verwaltungsdienst in einem Speicherblob unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd073-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="dd073-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dd073-111">PARAMETERS</span></span>

### <span data-ttu-id="dd073-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd073-112">-DefaultProfile</span></span>
<span data-ttu-id="dd073-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd073-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd073-114">-Name</span><span class="sxs-lookup"><span data-stu-id="dd073-114">-Name</span></span>
<span data-ttu-id="dd073-115">Gibt den Namen der API-Verwaltungsbereitstellung an, die von diesem Cmdlet unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dd073-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="dd073-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd073-116">-PassThru</span></span>
<span data-ttu-id="dd073-117">Gibt an, dass dieses Cmdlet das gesicherte **PsApiManagement-Objekt** zurückgibt, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="dd073-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="dd073-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd073-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd073-119">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungsbereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dd073-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="dd073-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dd073-120">-StorageContext</span></span>
<span data-ttu-id="dd073-121">Gibt einen Speicherverbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="dd073-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd073-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="dd073-122">-TargetBlobName</span></span>
<span data-ttu-id="dd073-123">Gibt den Namen des Blobs für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="dd073-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="dd073-124">Wenn das Blob nicht vorhanden ist, wird es von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd073-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="dd073-125">Dieses Cmdlet generiert einen Standardwert basierend auf dem folgenden Muster: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span><span class="sxs-lookup"><span data-stu-id="dd073-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd073-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="dd073-126">-TargetContainerName</span></span>
<span data-ttu-id="dd073-127">Gibt den Namen des Containers des Blobs für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="dd073-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="dd073-128">Wenn der Container nicht vorhanden ist, wird er von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="dd073-128">If the container does not exist, this cmdlet creates it.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd073-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd073-129">CommonParameters</span></span>
<span data-ttu-id="dd073-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd073-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd073-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd073-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd073-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd073-132">INPUTS</span></span>

### <span data-ttu-id="dd073-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dd073-133">System.String</span></span>

### <span data-ttu-id="dd073-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd073-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd073-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd073-135">OUTPUTS</span></span>

### <span data-ttu-id="dd073-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd073-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dd073-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dd073-137">NOTES</span></span>

## <span data-ttu-id="dd073-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dd073-138">RELATED LINKS</span></span>

[<span data-ttu-id="dd073-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd073-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="dd073-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd073-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="dd073-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd073-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="dd073-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd073-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


