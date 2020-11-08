---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006769"
---
# <span data-ttu-id="263cb-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="263cb-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="263cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="263cb-102">SYNOPSIS</span></span>
<span data-ttu-id="263cb-103">Ruft die Größen-und Größenbeschränkung einer SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="263cb-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="263cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="263cb-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="263cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="263cb-105">DESCRIPTION</span></span>
<span data-ttu-id="263cb-106">Das Cmdlet " **Get-AzureSqlDatabaseUsages** " Ruft die aktuelle Größe und Größenbeschränkung einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="263cb-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="263cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="263cb-107">EXAMPLES</span></span>

### <span data-ttu-id="263cb-108">Beispiel 1: Abrufen von Nutzungsinformationen für eine SQL-Datenbank</span><span class="sxs-lookup"><span data-stu-id="263cb-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="263cb-109">Dieser Befehl ruft die Größen-und Größen Beschränkungsinformationen für die SQL-Datenbank mit dem Namen Database01 auf SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="263cb-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="263cb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="263cb-110">PARAMETERS</span></span>

### <span data-ttu-id="263cb-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="263cb-111">-DatabaseName</span></span>
<span data-ttu-id="263cb-112">Gibt den Namen der Azure SQL-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="263cb-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263cb-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="263cb-113">-Profile</span></span>
<span data-ttu-id="263cb-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="263cb-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="263cb-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="263cb-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263cb-116">-Servername</span><span class="sxs-lookup"><span data-stu-id="263cb-116">-ServerName</span></span>
<span data-ttu-id="263cb-117">Gibt den Namen des Servers an, der die Azure SQL-Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="263cb-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263cb-118">CommonParameters</span></span>
<span data-ttu-id="263cb-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263cb-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="263cb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263cb-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="263cb-121">INPUTS</span></span>

## <span data-ttu-id="263cb-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="263cb-122">OUTPUTS</span></span>

## <span data-ttu-id="263cb-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="263cb-123">NOTES</span></span>

## <span data-ttu-id="263cb-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="263cb-124">RELATED LINKS</span></span>

