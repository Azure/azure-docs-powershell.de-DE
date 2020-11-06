---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: ce6bd748a639116f1f6d2e5c42e824fb3687bdfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502125"
---
# <span data-ttu-id="48394-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="48394-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="48394-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48394-102">SYNOPSIS</span></span>
<span data-ttu-id="48394-103">Erstellt einen Data Lake-Analyse Katalog Secret.</span><span class="sxs-lookup"><span data-stu-id="48394-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48394-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48394-104">SYNTAX</span></span>

### <span data-ttu-id="48394-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="48394-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48394-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="48394-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48394-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48394-107">DESCRIPTION</span></span>
<span data-ttu-id="48394-108">Das Cmdlet **New-AzureRmDataLakeAnalyticsCatalogSecret** erstellt einen Schlüssel, der in einem Azure Data Lake-Analyse Katalog verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="48394-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="48394-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48394-109">EXAMPLES</span></span>

### <span data-ttu-id="48394-110">Beispiel 1: Abrufen des Schlüssels für einen Katalog</span><span class="sxs-lookup"><span data-stu-id="48394-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="48394-111">Dieser Befehl ruft den geheimen Schlüssel ab, der dem angegebenen Konto, der angegebenen Datenbank, den angegebenen Anmeldeinformationen und dem angegebenen Host entspricht.</span><span class="sxs-lookup"><span data-stu-id="48394-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="48394-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="48394-112">PARAMETERS</span></span>

### <span data-ttu-id="48394-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="48394-113">-Account</span></span>
<span data-ttu-id="48394-114">Gibt den Namen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="48394-114">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48394-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="48394-115">-DatabaseHost</span></span>
<span data-ttu-id="48394-116">Gibt den Hostnamen für die Datenbank an, der der Schlüssel im Format "MyDatabase.contoso.com" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="48394-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48394-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="48394-117">-DatabaseName</span></span>
<span data-ttu-id="48394-118">Gibt den Namen der Datenbank an, die den geheimen Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="48394-118">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48394-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48394-119">-DefaultProfile</span></span>
<span data-ttu-id="48394-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="48394-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48394-121">-Port</span><span class="sxs-lookup"><span data-stu-id="48394-121">-Port</span></span>
<span data-ttu-id="48394-122">Gibt die Portnummer des Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="48394-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48394-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="48394-123">-Secret</span></span>
<span data-ttu-id="48394-124">Gibt den Namen und das Kennwort für den geheimen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="48394-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48394-125">-URI</span><span class="sxs-lookup"><span data-stu-id="48394-125">-Uri</span></span>
<span data-ttu-id="48394-126">Gibt den Uniform Resource Identifier (URI) des Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="48394-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48394-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48394-127">CommonParameters</span></span>
<span data-ttu-id="48394-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48394-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48394-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48394-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48394-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48394-130">INPUTS</span></span>

### <span data-ttu-id="48394-131">System. String</span><span class="sxs-lookup"><span data-stu-id="48394-131">System.String</span></span>

### <span data-ttu-id="48394-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="48394-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="48394-133">System. Uri</span><span class="sxs-lookup"><span data-stu-id="48394-133">System.Uri</span></span>

### <span data-ttu-id="48394-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="48394-134">System.Int32</span></span>

## <span data-ttu-id="48394-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48394-135">OUTPUTS</span></span>

### <span data-ttu-id="48394-136">Microsoft. Azure. Management. datalake. Analytics. Models. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="48394-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="48394-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="48394-137">NOTES</span></span>

## <span data-ttu-id="48394-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48394-138">RELATED LINKS</span></span>

[<span data-ttu-id="48394-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="48394-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="48394-140">Satz-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="48394-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


