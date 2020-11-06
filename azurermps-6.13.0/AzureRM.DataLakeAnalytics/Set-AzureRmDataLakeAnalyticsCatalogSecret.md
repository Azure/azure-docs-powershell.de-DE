---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CAB32C72-5C16-467E-BC57-749EC49916BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 22a10d4f65d43f4d11871cbf43399bfc35febf04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502965"
---
# <span data-ttu-id="aa5d1-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="aa5d1-101">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="aa5d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="aa5d1-103">Ändert einen Geheimtipp des Daten Lake Analytics-Katalogs.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-103">Modifies a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa5d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5d1-104">SYNTAX</span></span>

### <span data-ttu-id="aa5d1-105">SetByFullUri</span><span class="sxs-lookup"><span data-stu-id="aa5d1-105">SetByFullUri</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa5d1-106">SetByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="aa5d1-106">SetByHostNameAndPort</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa5d1-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa5d1-107">DESCRIPTION</span></span>
<span data-ttu-id="aa5d1-108">Das Cmdlet " **Satz-AzureRmDataLakeAnalyticsCatalogSecret** " ändert einen geheimen Schlüssel, der einem Azure Data Lake-Analyse Katalog zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-108">The **Set-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet modifies a secret associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="aa5d1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa5d1-109">EXAMPLES</span></span>

### <span data-ttu-id="aa5d1-110">Beispiel 1: Ändern des mit einem Konto verknüpften Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="aa5d1-110">Example 1: Modify the secret associated with an account</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="aa5d1-111">Mit diesem Befehl wird der mit einem Data Lake Analytics-Katalog verknüpfte geheim Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-111">This command sets the secret associated with a Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="aa5d1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa5d1-112">PARAMETERS</span></span>

### <span data-ttu-id="aa5d1-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="aa5d1-113">-Account</span></span>
<span data-ttu-id="aa5d1-114">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="aa5d1-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="aa5d1-115">-DatabaseHost</span></span>
<span data-ttu-id="aa5d1-116">Gibt den Hostnamen für die Datenbank an, der der Schlüssel im Format "MyDatabase.contoso.com" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullUri
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5d1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="aa5d1-117">-DatabaseName</span></span>
<span data-ttu-id="aa5d1-118">Gibt den Namen der Datenbank an, die den geheimen Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-118">Specifies the name of the database holding the secret.</span></span>

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

### <span data-ttu-id="aa5d1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa5d1-119">-DefaultProfile</span></span>
<span data-ttu-id="aa5d1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="aa5d1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa5d1-121">-Port</span><span class="sxs-lookup"><span data-stu-id="aa5d1-121">-Port</span></span>
<span data-ttu-id="aa5d1-122">Gibt die Portnummer des Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullUri
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5d1-123">-Secret</span><span class="sxs-lookup"><span data-stu-id="aa5d1-123">-Secret</span></span>
<span data-ttu-id="aa5d1-124">Gibt den Namen und das Kennwort für den geheimen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-124">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="aa5d1-125">-URI</span><span class="sxs-lookup"><span data-stu-id="aa5d1-125">-Uri</span></span>
<span data-ttu-id="aa5d1-126">Gibt den Uniform Resource Identifier (URI) für den geheimen Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-126">Specifies the Uniform Resource Identifier (URI) for the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa5d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa5d1-127">CommonParameters</span></span>
<span data-ttu-id="aa5d1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa5d1-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa5d1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa5d1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa5d1-130">INPUTS</span></span>

### <span data-ttu-id="aa5d1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="aa5d1-131">System.String</span></span>

### <span data-ttu-id="aa5d1-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="aa5d1-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="aa5d1-133">System. Uri</span><span class="sxs-lookup"><span data-stu-id="aa5d1-133">System.Uri</span></span>

### <span data-ttu-id="aa5d1-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="aa5d1-134">System.Int32</span></span>

## <span data-ttu-id="aa5d1-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa5d1-135">OUTPUTS</span></span>

### <span data-ttu-id="aa5d1-136">Microsoft. Azure. Management. datalake. Analytics. Models. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="aa5d1-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="aa5d1-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa5d1-137">NOTES</span></span>

## <span data-ttu-id="aa5d1-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa5d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="aa5d1-139">Neu – AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="aa5d1-139">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="aa5d1-140">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="aa5d1-140">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)


