---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006394"
---
# <span data-ttu-id="a21d3-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="a21d3-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="a21d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a21d3-102">SYNOPSIS</span></span>

## <span data-ttu-id="a21d3-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="a21d3-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a21d3-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a21d3-104">DESCRIPTION</span></span>

## <span data-ttu-id="a21d3-105">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a21d3-105">EXAMPLES</span></span>

### <span data-ttu-id="a21d3-106">1:</span><span class="sxs-lookup"><span data-stu-id="a21d3-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="a21d3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a21d3-107">PARAMETERS</span></span>

### <span data-ttu-id="a21d3-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="a21d3-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21d3-109">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="a21d3-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21d3-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="a21d3-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21d3-111">-Information</span><span class="sxs-lookup"><span data-stu-id="a21d3-111">-InformationAction</span></span>
<span data-ttu-id="a21d3-112">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a21d3-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a21d3-113">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a21d3-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a21d3-114">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a21d3-114">Continue</span></span>
- <span data-ttu-id="a21d3-115">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a21d3-115">Ignore</span></span>
- <span data-ttu-id="a21d3-116">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a21d3-116">Inquire</span></span>
- <span data-ttu-id="a21d3-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a21d3-117">SilentlyContinue</span></span>
- <span data-ttu-id="a21d3-118">Beenden</span><span class="sxs-lookup"><span data-stu-id="a21d3-118">Stop</span></span>
- <span data-ttu-id="a21d3-119">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a21d3-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a21d3-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a21d3-120">-InformationVariable</span></span>
<span data-ttu-id="a21d3-121">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a21d3-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a21d3-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="a21d3-122">-Profile</span></span>
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

### <span data-ttu-id="a21d3-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a21d3-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21d3-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="a21d3-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21d3-125">CommonParameters</span></span>
<span data-ttu-id="a21d3-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a21d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21d3-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a21d3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21d3-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a21d3-128">INPUTS</span></span>

## <span data-ttu-id="a21d3-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a21d3-129">OUTPUTS</span></span>

## <span data-ttu-id="a21d3-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="a21d3-130">NOTES</span></span>

## <span data-ttu-id="a21d3-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a21d3-131">RELATED LINKS</span></span>

