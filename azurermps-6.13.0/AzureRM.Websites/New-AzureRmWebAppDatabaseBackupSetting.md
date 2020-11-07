---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 958b8eb85084514817e36c5b61d1cd8bd567dbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664297"
---
# <span data-ttu-id="5d50d-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="5d50d-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="5d50d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d50d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d50d-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d50d-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d50d-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d50d-104">DESCRIPTION</span></span>
<span data-ttu-id="5d50d-105">Das Cmdlet **New-AzureRmWebAppDatabaseBackupSetting** erstellt eine neue Azure Web App-Sicherungseinstellung.</span><span class="sxs-lookup"><span data-stu-id="5d50d-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="5d50d-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d50d-106">EXAMPLES</span></span>

### <span data-ttu-id="5d50d-107">1:</span><span class="sxs-lookup"><span data-stu-id="5d50d-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="5d50d-108">Erstellt eine Daten Bank Sicherungseinstellung (Verbindungszeichenfolge) vom Typ sqlazure für die angegebene App-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe-Web-westus befindet.</span><span class="sxs-lookup"><span data-stu-id="5d50d-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5d50d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d50d-109">PARAMETERS</span></span>

### <span data-ttu-id="5d50d-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5d50d-110">-ConnectionString</span></span>
<span data-ttu-id="5d50d-111">Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5d50d-111">Connection String</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d50d-112">-ConnectionStringName</span><span class="sxs-lookup"><span data-stu-id="5d50d-112">-ConnectionStringName</span></span>
<span data-ttu-id="5d50d-113">Name der Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5d50d-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d50d-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="5d50d-114">-DatabaseType</span></span>
<span data-ttu-id="5d50d-115">Datenbank-Typ (z.b. "sqlazure" oder "MySQL")</span><span class="sxs-lookup"><span data-stu-id="5d50d-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="5d50d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d50d-116">-DefaultProfile</span></span>
<span data-ttu-id="5d50d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d50d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d50d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5d50d-118">-Name</span></span>
<span data-ttu-id="5d50d-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="5d50d-119">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d50d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d50d-120">CommonParameters</span></span>
<span data-ttu-id="5d50d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d50d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d50d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d50d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d50d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d50d-123">INPUTS</span></span>

### <span data-ttu-id="5d50d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5d50d-124">System.String</span></span>

## <span data-ttu-id="5d50d-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d50d-125">OUTPUTS</span></span>

### <span data-ttu-id="5d50d-126">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="5d50d-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="5d50d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d50d-127">NOTES</span></span>

## <span data-ttu-id="5d50d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d50d-128">RELATED LINKS</span></span>
