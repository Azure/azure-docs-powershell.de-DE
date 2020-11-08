---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175317"
---
# <span data-ttu-id="0bee3-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0bee3-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="0bee3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0bee3-102">SYNOPSIS</span></span>
<span data-ttu-id="0bee3-103">Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="0bee3-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="0bee3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bee3-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bee3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bee3-105">DESCRIPTION</span></span>
<span data-ttu-id="0bee3-106">Mit dem Cmdlet " **Backup-AzApiManagement** " wird eine Instanz eines Azure API-Verwaltungsdiensts gesichert.</span><span class="sxs-lookup"><span data-stu-id="0bee3-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="0bee3-107">Dieses Cmdlet speichert die Sicherung als Azure-Speicher-BLOB.</span><span class="sxs-lookup"><span data-stu-id="0bee3-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="0bee3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0bee3-108">EXAMPLES</span></span>

### <span data-ttu-id="0bee3-109">Beispiel 1: Sichern eines API-Verwaltungsdiensts</span><span class="sxs-lookup"><span data-stu-id="0bee3-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="0bee3-110">Mit diesem Befehl wird ein API-Verwaltungsdienst zu einem Speicher-BLOB gesichert.</span><span class="sxs-lookup"><span data-stu-id="0bee3-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="0bee3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bee3-111">PARAMETERS</span></span>

### <span data-ttu-id="0bee3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bee3-112">-DefaultProfile</span></span>
<span data-ttu-id="0bee3-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0bee3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bee3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0bee3-114">-Name</span></span>
<span data-ttu-id="0bee3-115">Gibt den Namen der API-Verwaltungs Bereitstellung an, die von diesem Cmdlet gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="0bee3-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="0bee3-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bee3-116">-PassThru</span></span>
<span data-ttu-id="0bee3-117">Gibt an, dass dieses Cmdlet das gesicherte **PsApiManagement** -Objekt zurückgibt, wenn der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0bee3-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="0bee3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bee3-118">-ResourceGroupName</span></span>
<span data-ttu-id="0bee3-119">Gibt den Namen der Ressourcengruppe an, unter der die API-Verwaltungs Bereitstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0bee3-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="0bee3-120">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="0bee3-120">-StorageContext</span></span>
<span data-ttu-id="0bee3-121">Gibt einen Speicher Verbindungskontext an.</span><span class="sxs-lookup"><span data-stu-id="0bee3-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="0bee3-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="0bee3-122">-TargetBlobName</span></span>
<span data-ttu-id="0bee3-123">Gibt den Namen des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="0bee3-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="0bee3-124">Wenn das BLOB nicht vorhanden ist, wird es von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="0bee3-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="0bee3-125">Dieses Cmdlet generiert einen Standardwert auf der Grundlage des folgenden Musters: {Name}-{yyyy-mm-dd-hh-mm}. apimbackup</span><span class="sxs-lookup"><span data-stu-id="0bee3-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="0bee3-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="0bee3-126">-TargetContainerName</span></span>
<span data-ttu-id="0bee3-127">Gibt den Namen des Containers des BLOB für die Sicherung an.</span><span class="sxs-lookup"><span data-stu-id="0bee3-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="0bee3-128">Wenn der Container nicht vorhanden ist, wird er von diesem Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="0bee3-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="0bee3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bee3-129">CommonParameters</span></span>
<span data-ttu-id="0bee3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bee3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bee3-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bee3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bee3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0bee3-132">INPUTS</span></span>

### <span data-ttu-id="0bee3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0bee3-133">System.String</span></span>

### <span data-ttu-id="0bee3-134">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0bee3-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0bee3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0bee3-135">OUTPUTS</span></span>

### <span data-ttu-id="0bee3-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0bee3-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0bee3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="0bee3-137">NOTES</span></span>

## <span data-ttu-id="0bee3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0bee3-138">RELATED LINKS</span></span>

[<span data-ttu-id="0bee3-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0bee3-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="0bee3-140">Neu – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0bee3-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="0bee3-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0bee3-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="0bee3-142">Wiederherstellen – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0bee3-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


