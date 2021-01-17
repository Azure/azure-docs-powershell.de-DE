---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471521"
---
# <span data-ttu-id="396cb-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="396cb-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="396cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="396cb-102">SYNOPSIS</span></span>
<span data-ttu-id="396cb-103">Unterstützt einen API-Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="396cb-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="396cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="396cb-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="396cb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="396cb-105">DESCRIPTION</span></span>
<span data-ttu-id="396cb-106">Das **Cmdlet "Backup-AzApiManagement"** gesichert eine Instanz eines Azure API-Verwaltungsdiensts.</span><span class="sxs-lookup"><span data-stu-id="396cb-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="396cb-107">Dieses Cmdlet speichert die Sicherung als Azure Storage-BLOB.</span><span class="sxs-lookup"><span data-stu-id="396cb-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="396cb-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="396cb-108">EXAMPLES</span></span>

### <span data-ttu-id="396cb-109">Beispiel 1: Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="396cb-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="396cb-110">Mit diesem Befehl wird ein API-Verwaltungsdienst in einem Speicher-BLOB sichern.</span><span class="sxs-lookup"><span data-stu-id="396cb-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="396cb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="396cb-111">PARAMETERS</span></span>

### <span data-ttu-id="396cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396cb-112">-DefaultProfile</span></span>
<span data-ttu-id="396cb-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="396cb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="396cb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="396cb-114">-Name</span></span>
<span data-ttu-id="396cb-115">Gibt den Namen der API-Verwaltungsbereitstellung an, die von diesem Cmdlet sichern wird.</span><span class="sxs-lookup"><span data-stu-id="396cb-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="396cb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="396cb-116">-PassThru</span></span>
<span data-ttu-id="396cb-117">Gibt an, dass dieses Cmdlet das gesicherte **"PsApiManagement"-Objekt** zurückgibt, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="396cb-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="396cb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396cb-118">-ResourceGroupName</span></span>
<span data-ttu-id="396cb-119">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungsbereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="396cb-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="396cb-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="396cb-120">-StorageContext</span></span>
<span data-ttu-id="396cb-121">Gibt einen Speicherverbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="396cb-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="396cb-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="396cb-122">-TargetBlobName</span></span>
<span data-ttu-id="396cb-123">Gibt den Namen des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="396cb-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="396cb-124">Wenn das BLOB nicht vorhanden ist, wird es von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="396cb-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="396cb-125">Dieses Cmdlet generiert einen Standardwert basierend auf dem folgenden Muster: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span><span class="sxs-lookup"><span data-stu-id="396cb-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="396cb-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="396cb-126">-TargetContainerName</span></span>
<span data-ttu-id="396cb-127">Gibt den Namen des Containers des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="396cb-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="396cb-128">Wenn der Container nicht vorhanden ist, wird er von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="396cb-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="396cb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396cb-129">CommonParameters</span></span>
<span data-ttu-id="396cb-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396cb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396cb-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="396cb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396cb-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="396cb-132">INPUTS</span></span>

### <span data-ttu-id="396cb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="396cb-133">System.String</span></span>

### <span data-ttu-id="396cb-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="396cb-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="396cb-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="396cb-135">OUTPUTS</span></span>

### <span data-ttu-id="396cb-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="396cb-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="396cb-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="396cb-137">NOTES</span></span>

## <span data-ttu-id="396cb-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="396cb-138">RELATED LINKS</span></span>

[<span data-ttu-id="396cb-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="396cb-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="396cb-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="396cb-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="396cb-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="396cb-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="396cb-142">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="396cb-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


