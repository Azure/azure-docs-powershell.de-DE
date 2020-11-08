---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996664"
---
# <span data-ttu-id="69eaa-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="69eaa-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="69eaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="69eaa-103">Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="69eaa-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="69eaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69eaa-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69eaa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="69eaa-106">Mit dem Cmdlet " **Backup-AzApiManagement** " wird eine Instanz eines Azure API-Verwaltungsdiensts gesichert.</span><span class="sxs-lookup"><span data-stu-id="69eaa-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="69eaa-107">Dieses Cmdlet speichert die Sicherung als Azure-Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="69eaa-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="69eaa-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69eaa-108">EXAMPLES</span></span>

### <span data-ttu-id="69eaa-109">Beispiel 1: Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="69eaa-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="69eaa-110">Mit diesem Befehl wird ein API-Verwaltungsdienst zu einem Speicher-BLOB gesichert.</span><span class="sxs-lookup"><span data-stu-id="69eaa-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="69eaa-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="69eaa-111">PARAMETERS</span></span>

### <span data-ttu-id="69eaa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69eaa-112">-DefaultProfile</span></span>
<span data-ttu-id="69eaa-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69eaa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69eaa-114">-Name</span><span class="sxs-lookup"><span data-stu-id="69eaa-114">-Name</span></span>
<span data-ttu-id="69eaa-115">Gibt den Namen der API-Verwaltungs Bereitstellung an, die von diesem Cmdlet gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="69eaa-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="69eaa-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69eaa-116">-PassThru</span></span>
<span data-ttu-id="69eaa-117">Gibt an, dass dieses Cmdlet das gesicherte **PsApiManagement** -Objekt zurückgibt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="69eaa-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="69eaa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69eaa-118">-ResourceGroupName</span></span>
<span data-ttu-id="69eaa-119">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="69eaa-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="69eaa-120">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="69eaa-120">-StorageContext</span></span>
<span data-ttu-id="69eaa-121">Gibt einen Speicher Verbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="69eaa-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="69eaa-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="69eaa-122">-TargetBlobName</span></span>
<span data-ttu-id="69eaa-123">Gibt den Namen des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="69eaa-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="69eaa-124">Wenn das BLOB nicht vorhanden ist, wird es von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="69eaa-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="69eaa-125">Dieses Cmdlet generiert einen Standardwert auf der Grundlage des folgenden Musters: {Name}-{yyyy-mm-dd-hh-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="69eaa-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="69eaa-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="69eaa-126">-TargetContainerName</span></span>
<span data-ttu-id="69eaa-127">Gibt den Namen des Containers des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="69eaa-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="69eaa-128">Wenn der Container nicht vorhanden ist, wird er von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="69eaa-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="69eaa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69eaa-129">CommonParameters</span></span>
<span data-ttu-id="69eaa-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69eaa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69eaa-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69eaa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69eaa-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69eaa-132">INPUTS</span></span>

### <span data-ttu-id="69eaa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="69eaa-133">System.String</span></span>

### <span data-ttu-id="69eaa-134">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="69eaa-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="69eaa-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69eaa-135">OUTPUTS</span></span>

### <span data-ttu-id="69eaa-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="69eaa-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="69eaa-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="69eaa-137">NOTES</span></span>

## <span data-ttu-id="69eaa-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69eaa-138">RELATED LINKS</span></span>

[<span data-ttu-id="69eaa-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="69eaa-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="69eaa-140">Neu – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="69eaa-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="69eaa-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="69eaa-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="69eaa-142">Wiederherstellen – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="69eaa-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


