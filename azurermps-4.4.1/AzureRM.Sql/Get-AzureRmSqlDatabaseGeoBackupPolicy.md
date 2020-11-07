---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: b8f7d04a709ebb14ed6a7a76cffab556c13d26ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664967"
---
# <span data-ttu-id="b61fd-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b61fd-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="b61fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b61fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b61fd-103">Ruft eine Daten Bank Geo-Sicherungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="b61fd-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b61fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b61fd-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b61fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b61fd-105">DESCRIPTION</span></span>
<span data-ttu-id="b61fd-106">Das Cmdlet " **Get-AzureRmSqlDatabaseGeoBackupPolicy** " Ruft die für diese Datenbank registrierte Geo-Sicherungsrichtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="b61fd-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="b61fd-107">Hierbei handelt es sich um eine Azure-Sicherungs Ressource, die zum Definieren von Sicherungsspeicher Richtlinien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b61fd-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="b61fd-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b61fd-108">EXAMPLES</span></span>

## <span data-ttu-id="b61fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b61fd-109">PARAMETERS</span></span>

### <span data-ttu-id="b61fd-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b61fd-110">-DatabaseName</span></span>
<span data-ttu-id="b61fd-111">Gibt den Namen der Datenbank an, für die dieses Cmdlet die Geo-Sicherungsrichtlinie erhält.</span><span class="sxs-lookup"><span data-stu-id="b61fd-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

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

### <span data-ttu-id="b61fd-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61fd-112">-ResourceGroupName</span></span>
<span data-ttu-id="b61fd-113">Gibt den Namen der Ressourcengruppe des Servers an, der diese Datenbank enthält.</span><span class="sxs-lookup"><span data-stu-id="b61fd-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b61fd-114">-Servername</span><span class="sxs-lookup"><span data-stu-id="b61fd-114">-ServerName</span></span>
<span data-ttu-id="b61fd-115">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="b61fd-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b61fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61fd-116">-DefaultProfile</span></span>
<span data-ttu-id="b61fd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b61fd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b61fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61fd-118">CommonParameters</span></span>
<span data-ttu-id="b61fd-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61fd-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61fd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61fd-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b61fd-121">INPUTS</span></span>

## <span data-ttu-id="b61fd-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b61fd-122">OUTPUTS</span></span>

## <span data-ttu-id="b61fd-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="b61fd-123">NOTES</span></span>

## <span data-ttu-id="b61fd-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b61fd-124">RELATED LINKS</span></span>

[<span data-ttu-id="b61fd-125">Satz-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b61fd-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="b61fd-126">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="b61fd-126">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
